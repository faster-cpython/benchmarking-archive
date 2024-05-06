# Results vs. 3.12.0

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 8eee1b4
- commit date: 2024-04-02
- overall geometric mean: 1.01x faster
- HPT reliability: 80.23%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 279 ms: 1.02x slower                                              |
| chameleon      | 7.41 ms                                                | 6.88 ms: 1.08x faster                                             |
| docutils       | 2.77 sec                                               | 2.91 sec: 1.05x slower                                            |
| tornado_http   | 103 ms                                                 | 95.7 ms: 1.07x faster                                             |
| Geometric mean | (ref)                                                  | 1.02x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 334 ms: 1.35x faster                                              |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                              |
| async_tree_memoization_tg  | 575 ms                                                 | 444 ms: 1.29x faster                                              |
| async_tree_memoization     | 578 ms                                                 | 455 ms: 1.27x faster                                              |
| async_tree_io_tg           | 1.18 sec                                               | 945 ms: 1.25x faster                                              |
| async_tree_io              | 1.16 sec                                               | 933 ms: 1.24x faster                                              |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 602 ms: 1.20x faster                                              |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 609 ms: 1.19x faster                                              |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 84.7 ms                                                | 78.1 ms: 1.08x faster                                             |
| nbody          | 97.0 ms                                                | 91.9 ms: 1.05x faster                                             |
| pidigits       | 187 ms                                                 | 194 ms: 1.03x slower                                              |
| Geometric mean | (ref)                                                  | 1.03x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 145 ms: 1.02x faster                                              |
| regex_effbot   | 3.61 ms                                                | 3.75 ms: 1.04x slower                                             |
| regex_dna      | 212 ms                                                 | 233 ms: 1.10x slower                                              |
| regex_v8       | 23.1 ms                                                | 26.1 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.06x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.07 sec: 1.13x faster                                            |
| pickle_pure_python   | 324 us                                                 | 304 us: 1.07x faster                                              |
| pickle_dict          | 35.5 us                                                | 34.1 us: 1.04x faster                                             |
| xml_etree_generate   | 89.2 ms                                                | 87.4 ms: 1.02x faster                                             |
| xml_etree_process    | 61.7 ms                                                | 60.6 ms: 1.02x faster                                             |
| unpickle_list        | 5.29 us                                                | 5.24 us: 1.01x faster                                             |
| pickle_list          | 5.08 us                                                | 5.06 us: 1.01x faster                                             |
| unpickle             | 15.9 us                                                | 15.9 us: 1.01x slower                                             |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                             |
| pickle               | 11.6 us                                                | 11.8 us: 1.01x slower                                             |
| xml_etree_parse      | 159 ms                                                 | 162 ms: 1.02x slower                                              |
| unpickle_pure_python | 230 us                                                 | 240 us: 1.04x slower                                              |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (2): json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.16x slower                                             |
| python_startup_no_site | 6.94 ms                                                | 9.55 ms: 1.38x slower                                             |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|-----------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 10.9 ms: 1.10x faster                                             |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 113 us: 1.39x faster                                              |
| async_tree_none_tg         | 450 ms                                                 | 334 ms: 1.35x faster                                              |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                              |
| async_tree_memoization_tg  | 575 ms                                                 | 444 ms: 1.29x faster                                              |
| async_tree_memoization     | 578 ms                                                 | 455 ms: 1.27x faster                                              |
| async_tree_io_tg           | 1.18 sec                                               | 945 ms: 1.25x faster                                              |
| async_tree_io              | 1.16 sec                                               | 933 ms: 1.24x faster                                              |
| comprehensions             | 21.8 us                                                | 17.8 us: 1.22x faster                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 602 ms: 1.20x faster                                              |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 609 ms: 1.19x faster                                              |
| scimark_fft                | 382 ms                                                 | 338 ms: 1.13x faster                                              |
| tomli_loads                | 2.33 sec                                               | 2.07 sec: 1.13x faster                                            |
| raytrace                   | 312 ms                                                 | 278 ms: 1.12x faster                                              |
| logging_format             | 7.23 us                                                | 6.59 us: 1.10x faster                                             |
| mako                       | 11.9 ms                                                | 10.9 ms: 1.10x faster                                             |
| scimark_monte_carlo        | 75.1 ms                                                | 68.7 ms: 1.09x faster                                             |
| crypto_pyaes               | 81.9 ms                                                | 75.4 ms: 1.09x faster                                             |
| chaos                      | 67.0 ms                                                | 61.7 ms: 1.09x faster                                             |
| float                      | 84.7 ms                                                | 78.1 ms: 1.08x faster                                             |
| chameleon                  | 7.41 ms                                                | 6.88 ms: 1.08x faster                                             |
| tornado_http               | 103 ms                                                 | 95.7 ms: 1.07x faster                                             |
| deepcopy_memo              | 40.7 us                                                | 38.0 us: 1.07x faster                                             |
| pickle_pure_python         | 324 us                                                 | 304 us: 1.07x faster                                              |
| logging_simple             | 6.46 us                                                | 6.08 us: 1.06x faster                                             |
| nbody                      | 97.0 ms                                                | 91.9 ms: 1.05x faster                                             |
| deepcopy                   | 371 us                                                 | 353 us: 1.05x faster                                              |
| generators                 | 31.2 ms                                                | 29.7 ms: 1.05x faster                                             |
| coroutines                 | 23.2 ms                                                | 22.1 ms: 1.05x faster                                             |
| fannkuch                   | 417 ms                                                 | 399 ms: 1.05x faster                                              |
| pickle_dict                | 35.5 us                                                | 34.1 us: 1.04x faster                                             |
| pprint_safe_repr           | 776 ms                                                 | 745 ms: 1.04x faster                                              |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.89 ms: 1.03x faster                                             |
| sqlglot_transpile          | 1.68 ms                                                | 1.63 ms: 1.03x faster                                             |
| deepcopy_reduce            | 3.35 us                                                | 3.24 us: 1.03x faster                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.32 ms: 1.03x faster                                             |
| logging_silent             | 104 ns                                                 | 101 ns: 1.03x faster                                              |
| regex_compile              | 148 ms                                                 | 145 ms: 1.02x faster                                              |
| xml_etree_generate         | 89.2 ms                                                | 87.4 ms: 1.02x faster                                             |
| xml_etree_process          | 61.7 ms                                                | 60.6 ms: 1.02x faster                                             |
| pprint_pformat             | 1.57 sec                                               | 1.54 sec: 1.02x faster                                            |
| pathlib                    | 19.3 ms                                                | 19.1 ms: 1.02x faster                                             |
| sympy_str                  | 300 ms                                                 | 295 ms: 1.02x faster                                              |
| spectral_norm              | 115 ms                                                 | 113 ms: 1.01x faster                                              |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.01x faster                                              |
| unpickle_list              | 5.29 us                                                | 5.24 us: 1.01x faster                                             |
| async_generators           | 463 ms                                                 | 459 ms: 1.01x faster                                              |
| pickle_list                | 5.08 us                                                | 5.06 us: 1.01x faster                                             |
| meteor_contest             | 112 ms                                                 | 112 ms: 1.00x faster                                              |
| unpickle                   | 15.9 us                                                | 15.9 us: 1.01x slower                                             |
| scimark_sor                | 129 ms                                                 | 130 ms: 1.01x slower                                              |
| deltablue                  | 3.72 ms                                                | 3.76 ms: 1.01x slower                                             |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                             |
| dask                       | 372 ms                                                 | 377 ms: 1.01x slower                                              |
| pickle                     | 11.6 us                                                | 11.8 us: 1.01x slower                                             |
| bench_thread_pool          | 842 us                                                 | 854 us: 1.01x slower                                              |
| 2to3                       | 274 ms                                                 | 279 ms: 1.02x slower                                              |
| xml_etree_parse            | 159 ms                                                 | 162 ms: 1.02x slower                                              |
| richards                   | 45.8 ms                                                | 46.7 ms: 1.02x slower                                             |
| sqlite_synth               | 2.83 us                                                | 2.89 us: 1.02x slower                                             |
| sqlglot_normalize          | 110 ms                                                 | 113 ms: 1.02x slower                                              |
| sympy_integrate            | 21.4 ms                                                | 21.9 ms: 1.02x slower                                             |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                              |
| mdp                        | 2.63 sec                                               | 2.70 sec: 1.02x slower                                            |
| json                       | 5.26 ms                                                | 5.39 ms: 1.03x slower                                             |
| pycparser                  | 1.18 sec                                               | 1.21 sec: 1.03x slower                                            |
| richards_super             | 51.5 ms                                                | 53.1 ms: 1.03x slower                                             |
| pidigits                   | 187 ms                                                 | 194 ms: 1.03x slower                                              |
| sympy_expand               | 478 ms                                                 | 496 ms: 1.04x slower                                              |
| regex_effbot               | 3.61 ms                                                | 3.75 ms: 1.04x slower                                             |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                            |
| dulwich_log                | 68.5 ms                                                | 71.3 ms: 1.04x slower                                             |
| unpickle_pure_python       | 230 us                                                 | 240 us: 1.04x slower                                              |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.04x slower                                             |
| asyncio_tcp                | 491 ms                                                 | 513 ms: 1.04x slower                                              |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                             |
| docutils                   | 2.77 sec                                               | 2.91 sec: 1.05x slower                                            |
| sqlglot_optimize           | 54.8 ms                                                | 57.6 ms: 1.05x slower                                             |
| nqueens                    | 83.3 ms                                                | 89.0 ms: 1.07x slower                                             |
| go                         | 139 ms                                                 | 150 ms: 1.07x slower                                              |
| hexiom                     | 6.41 ms                                                | 6.93 ms: 1.08x slower                                             |
| regex_dna                  | 212 ms                                                 | 233 ms: 1.10x slower                                              |
| scimark_lu                 | 118 ms                                                 | 131 ms: 1.11x slower                                              |
| regex_v8                   | 23.1 ms                                                | 26.1 ms: 1.13x slower                                             |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.16x slower                                             |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.18x slower                                             |
| telco                      | 7.10 ms                                                | 8.65 ms: 1.22x slower                                             |
| python_startup_no_site     | 6.94 ms                                                | 9.55 ms: 1.38x slower                                             |
| coverage                   | 72.7 ms                                                | 101 ms: 1.38x slower                                              |
| unpack_sequence            | 54.0 ns                                                | 89.6 ns: 1.66x slower                                             |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (6): mypy2, pyflate, bench_mp_pool, gc_traversal, json_loads, xml_etree_iterparse
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240402-3.13.0a5+-8eee1b4-JIT/bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 80.23% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x