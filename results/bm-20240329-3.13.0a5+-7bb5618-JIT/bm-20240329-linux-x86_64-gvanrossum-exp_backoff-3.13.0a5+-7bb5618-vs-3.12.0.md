# Results vs. 3.12.0

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 7bb5618
- commit date: 2024-03-29
- overall geometric mean: 1.00x faster
- HPT reliability: 56.24%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 281 ms: 1.02x slower                                              |
| chameleon      | 7.41 ms                                                | 7.19 ms: 1.03x faster                                             |
| docutils       | 2.77 sec                                               | 2.90 sec: 1.05x slower                                            |
| tornado_http   | 103 ms                                                 | 97.1 ms: 1.06x faster                                             |
| Geometric mean | (ref)                                                  | 1.00x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 342 ms: 1.31x faster                                              |
| async_tree_io_tg           | 1.18 sec                                               | 934 ms: 1.27x faster                                              |
| async_tree_memoization_tg  | 575 ms                                                 | 454 ms: 1.27x faster                                              |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                              |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 587 ms: 1.24x faster                                              |
| async_tree_io              | 1.16 sec                                               | 957 ms: 1.21x faster                                              |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 601 ms: 1.21x faster                                              |
| async_tree_none            | 472 ms                                                 | 391 ms: 1.21x faster                                              |
| Geometric mean             | (ref)                                                  | 1.24x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 84.7 ms                                                | 77.1 ms: 1.10x faster                                             |
| nbody          | 97.0 ms                                                | 90.6 ms: 1.07x faster                                             |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                              |
| Geometric mean | (ref)                                                  | 1.05x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 146 ms: 1.02x faster                                              |
| regex_effbot   | 3.61 ms                                                | 3.84 ms: 1.07x slower                                             |
| regex_dna      | 212 ms                                                 | 230 ms: 1.09x slower                                              |
| regex_v8       | 23.1 ms                                                | 25.8 ms: 1.11x slower                                             |
| Geometric mean | (ref)                                                  | 1.06x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.07 sec: 1.13x faster                                            |
| pickle_pure_python   | 324 us                                                 | 308 us: 1.05x faster                                              |
| pickle_list          | 5.08 us                                                | 4.93 us: 1.03x faster                                             |
| pickle_dict          | 35.5 us                                                | 34.6 us: 1.03x faster                                             |
| unpickle             | 15.9 us                                                | 15.7 us: 1.01x faster                                             |
| xml_etree_generate   | 89.2 ms                                                | 89.7 ms: 1.01x slower                                             |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.01x slower                                              |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                             |
| xml_etree_parse      | 159 ms                                                 | 162 ms: 1.02x slower                                              |
| unpickle_list        | 5.29 us                                                | 5.38 us: 1.02x slower                                             |
| pickle               | 11.6 us                                                | 12.0 us: 1.03x slower                                             |
| unpickle_pure_python | 230 us                                                 | 245 us: 1.07x slower                                              |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (2): xml_etree_process, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.0 ms: 1.16x slower                                             |
| python_startup_no_site | 6.94 ms                                                | 9.49 ms: 1.37x slower                                             |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.7 ms: 1.11x faster                                             |
| django_template | 34.6 ms                                                | 36.5 ms: 1.05x slower                                             |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 117 us: 1.35x faster                                              |
| async_tree_none_tg         | 450 ms                                                 | 342 ms: 1.31x faster                                              |
| async_tree_io_tg           | 1.18 sec                                               | 934 ms: 1.27x faster                                              |
| async_tree_memoization_tg  | 575 ms                                                 | 454 ms: 1.27x faster                                              |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                              |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 587 ms: 1.24x faster                                              |
| async_tree_io              | 1.16 sec                                               | 957 ms: 1.21x faster                                              |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 601 ms: 1.21x faster                                              |
| async_tree_none            | 472 ms                                                 | 391 ms: 1.21x faster                                              |
| comprehensions             | 21.8 us                                                | 18.3 us: 1.19x faster                                             |
| tomli_loads                | 2.33 sec                                               | 2.07 sec: 1.13x faster                                            |
| mako                       | 11.9 ms                                                | 10.7 ms: 1.11x faster                                             |
| scimark_fft                | 382 ms                                                 | 346 ms: 1.11x faster                                              |
| float                      | 84.7 ms                                                | 77.1 ms: 1.10x faster                                             |
| crypto_pyaes               | 81.9 ms                                                | 74.6 ms: 1.10x faster                                             |
| logging_format             | 7.23 us                                                | 6.61 us: 1.09x faster                                             |
| logging_simple             | 6.46 us                                                | 5.98 us: 1.08x faster                                             |
| nbody                      | 97.0 ms                                                | 90.6 ms: 1.07x faster                                             |
| tornado_http               | 103 ms                                                 | 97.1 ms: 1.06x faster                                             |
| scimark_monte_carlo        | 75.1 ms                                                | 71.2 ms: 1.06x faster                                             |
| fannkuch                   | 417 ms                                                 | 396 ms: 1.05x faster                                              |
| raytrace                   | 312 ms                                                 | 297 ms: 1.05x faster                                              |
| pickle_pure_python         | 324 us                                                 | 308 us: 1.05x faster                                              |
| deepcopy_reduce            | 3.35 us                                                | 3.21 us: 1.04x faster                                             |
| generators                 | 31.2 ms                                                | 30.1 ms: 1.04x faster                                             |
| coroutines                 | 23.2 ms                                                | 22.4 ms: 1.03x faster                                             |
| chameleon                  | 7.41 ms                                                | 7.19 ms: 1.03x faster                                             |
| pickle_list                | 5.08 us                                                | 4.93 us: 1.03x faster                                             |
| deepcopy                   | 371 us                                                 | 361 us: 1.03x faster                                              |
| pickle_dict                | 35.5 us                                                | 34.6 us: 1.03x faster                                             |
| deepcopy_memo              | 40.7 us                                                | 39.7 us: 1.03x faster                                             |
| sympy_str                  | 300 ms                                                 | 292 ms: 1.02x faster                                              |
| pprint_safe_repr           | 776 ms                                                 | 759 ms: 1.02x faster                                              |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.96 ms: 1.02x faster                                             |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.02x faster                                              |
| chaos                      | 67.0 ms                                                | 65.8 ms: 1.02x faster                                             |
| regex_compile              | 148 ms                                                 | 146 ms: 1.02x faster                                              |
| sqlglot_transpile          | 1.68 ms                                                | 1.66 ms: 1.02x faster                                             |
| pprint_pformat             | 1.57 sec                                               | 1.55 sec: 1.01x faster                                            |
| unpickle                   | 15.9 us                                                | 15.7 us: 1.01x faster                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.35 ms: 1.01x faster                                             |
| pathlib                    | 19.3 ms                                                | 19.1 ms: 1.01x faster                                             |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.01x faster                                              |
| gc_traversal               | 3.79 ms                                                | 3.78 ms: 1.00x faster                                             |
| xml_etree_generate         | 89.2 ms                                                | 89.7 ms: 1.01x slower                                             |
| async_generators           | 463 ms                                                 | 466 ms: 1.01x slower                                              |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.01x slower                                              |
| spectral_norm              | 115 ms                                                 | 116 ms: 1.01x slower                                              |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                             |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                              |
| mdp                        | 2.63 sec                                               | 2.67 sec: 1.01x slower                                            |
| xml_etree_parse            | 159 ms                                                 | 162 ms: 1.02x slower                                              |
| unpickle_list              | 5.29 us                                                | 5.38 us: 1.02x slower                                             |
| bench_thread_pool          | 842 us                                                 | 856 us: 1.02x slower                                              |
| dask                       | 372 ms                                                 | 378 ms: 1.02x slower                                              |
| json                       | 5.26 ms                                                | 5.36 ms: 1.02x slower                                             |
| sqlite_synth               | 2.83 us                                                | 2.89 us: 1.02x slower                                             |
| pyflate                    | 482 ms                                                 | 492 ms: 1.02x slower                                              |
| sympy_integrate            | 21.4 ms                                                | 21.9 ms: 1.02x slower                                             |
| 2to3                       | 274 ms                                                 | 281 ms: 1.02x slower                                              |
| scimark_sor                | 129 ms                                                 | 133 ms: 1.03x slower                                              |
| pickle                     | 11.6 us                                                | 12.0 us: 1.03x slower                                             |
| dulwich_log                | 68.5 ms                                                | 70.7 ms: 1.03x slower                                             |
| richards                   | 45.8 ms                                                | 47.3 ms: 1.03x slower                                             |
| asyncio_websockets         | 551 ms                                                 | 569 ms: 1.03x slower                                              |
| sqlglot_normalize          | 110 ms                                                 | 114 ms: 1.03x slower                                              |
| logging_silent             | 104 ns                                                 | 108 ns: 1.03x slower                                              |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.85 sec: 1.04x slower                                            |
| sympy_expand               | 478 ms                                                 | 498 ms: 1.04x slower                                              |
| asyncio_tcp                | 491 ms                                                 | 511 ms: 1.04x slower                                              |
| pycparser                  | 1.18 sec                                               | 1.23 sec: 1.04x slower                                            |
| docutils                   | 2.77 sec                                               | 2.90 sec: 1.05x slower                                            |
| richards_super             | 51.5 ms                                                | 53.9 ms: 1.05x slower                                             |
| gunicorn                   | 1.24 ms                                                | 1.31 ms: 1.05x slower                                             |
| django_template            | 34.6 ms                                                | 36.5 ms: 1.05x slower                                             |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.06x slower                                             |
| sqlglot_optimize           | 54.8 ms                                                | 58.0 ms: 1.06x slower                                             |
| deltablue                  | 3.72 ms                                                | 3.93 ms: 1.06x slower                                             |
| regex_effbot               | 3.61 ms                                                | 3.84 ms: 1.07x slower                                             |
| unpickle_pure_python       | 230 us                                                 | 245 us: 1.07x slower                                              |
| regex_dna                  | 212 ms                                                 | 230 ms: 1.09x slower                                              |
| nqueens                    | 83.3 ms                                                | 90.7 ms: 1.09x slower                                             |
| go                         | 139 ms                                                 | 153 ms: 1.10x slower                                              |
| hexiom                     | 6.41 ms                                                | 7.15 ms: 1.11x slower                                             |
| regex_v8                   | 23.1 ms                                                | 25.8 ms: 1.11x slower                                             |
| scimark_lu                 | 118 ms                                                 | 133 ms: 1.13x slower                                              |
| create_gc_cycles           | 1.48 ms                                                | 1.69 ms: 1.14x slower                                             |
| python_startup             | 9.55 ms                                                | 11.0 ms: 1.16x slower                                             |
| telco                      | 7.10 ms                                                | 8.71 ms: 1.23x slower                                             |
| python_startup_no_site     | 6.94 ms                                                | 9.49 ms: 1.37x slower                                             |
| coverage                   | 72.7 ms                                                | 99.8 ms: 1.37x slower                                             |
| unpack_sequence            | 54.0 ns                                                | 86.2 ns: 1.60x slower                                             |
| Geometric mean             | (ref)                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (4): mypy2, xml_etree_process, bench_mp_pool, json_loads
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (6) of results/bm-20240329-3.13.0a5+-7bb5618-JIT/bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 56.24% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.03x