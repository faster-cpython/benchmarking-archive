# Results vs. 3.12.0

- fork: gvanrossum
- ref: exp_backoff
- machine: darwin-arm64
- commit hash: dcee362
- commit date: 2024-04-03
- overall geometric mean: 1.03x faster
- HPT reliability: 99.08%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 171 ms: 1.01x slower                                              |
| chameleon      | 4.70 ms                                                | 4.47 ms: 1.05x faster                                             |
| docutils       | 1.50 sec                                               | 1.55 sec: 1.03x slower                                            |
| tornado_http   | 69.3 ms                                                | 80.2 ms: 1.16x slower                                             |
| Geometric mean | (ref)                                                  | 1.04x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none            | 266 ms                                                 | 202 ms: 1.31x faster                                              |
| async_tree_none_tg         | 258 ms                                                 | 197 ms: 1.31x faster                                              |
| async_tree_memoization_tg  | 323 ms                                                 | 260 ms: 1.24x faster                                              |
| async_tree_memoization     | 312 ms                                                 | 260 ms: 1.20x faster                                              |
| async_tree_io_tg           | 669 ms                                                 | 561 ms: 1.19x faster                                              |
| async_tree_io              | 668 ms                                                 | 564 ms: 1.18x faster                                              |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 454 ms: 1.17x faster                                              |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 464 ms: 1.13x faster                                              |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 55.8 ms                                                | 49.2 ms: 1.13x faster                                             |
| nbody          | 68.8 ms                                                | 70.7 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                  | 1.03x faster                                                      |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_dna      | 154 ms                                                 | 152 ms: 1.01x faster                                              |
| regex_effbot   | 2.64 ms                                                | 2.63 ms: 1.00x faster                                             |
| regex_v8       | 16.0 ms                                                | 17.2 ms: 1.08x slower                                             |
| regex_compile  | 77.9 ms                                                | 86.4 ms: 1.11x slower                                             |
| Geometric mean | (ref)                                                  | 1.04x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 182 us: 1.10x faster                                              |
| tomli_loads          | 1.39 sec                                               | 1.28 sec: 1.09x faster                                            |
| unpickle_pure_python | 151 us                                                 | 139 us: 1.08x faster                                              |
| xml_etree_process    | 39.7 ms                                                | 37.3 ms: 1.06x faster                                             |
| xml_etree_generate   | 55.8 ms                                                | 54.3 ms: 1.03x faster                                             |
| json_loads           | 17.2 us                                                | 16.9 us: 1.02x faster                                             |
| xml_etree_iterparse  | 74.0 ms                                                | 72.6 ms: 1.02x faster                                             |
| unpickle_list        | 3.02 us                                                | 3.00 us: 1.01x faster                                             |
| pickle_dict          | 18.1 us                                                | 18.2 us: 1.01x slower                                             |
| unpickle             | 9.12 us                                                | 9.28 us: 1.02x slower                                             |
| json_dumps           | 6.22 ms                                                | 6.33 ms: 1.02x slower                                             |
| pickle_list          | 2.89 us                                                | 2.96 us: 1.03x slower                                             |
| pickle               | 7.23 us                                                | 7.50 us: 1.04x slower                                             |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                      |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 11.4 ms                                                | 13.3 ms: 1.16x slower                                             |
| python_startup_no_site | 9.37 ms                                                | 11.6 ms: 1.24x slower                                             |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|-----------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako      | 7.71 ms                                                | 6.97 ms: 1.11x faster                                             |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 93.0 us                                                | 69.2 us: 1.34x faster                                             |
| async_tree_none            | 266 ms                                                 | 202 ms: 1.31x faster                                              |
| async_tree_none_tg         | 258 ms                                                 | 197 ms: 1.31x faster                                              |
| raytrace                   | 212 ms                                                 | 163 ms: 1.30x faster                                              |
| async_tree_memoization_tg  | 323 ms                                                 | 260 ms: 1.24x faster                                              |
| comprehensions             | 14.5 us                                                | 11.9 us: 1.22x faster                                             |
| logging_silent             | 76.4 ns                                                | 63.7 ns: 1.20x faster                                             |
| async_tree_memoization     | 312 ms                                                 | 260 ms: 1.20x faster                                              |
| async_tree_io_tg           | 669 ms                                                 | 561 ms: 1.19x faster                                              |
| async_tree_io              | 668 ms                                                 | 564 ms: 1.18x faster                                              |
| generators                 | 31.1 ms                                                | 26.3 ms: 1.18x faster                                             |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 454 ms: 1.17x faster                                              |
| logging_simple             | 3.69 us                                                | 3.15 us: 1.17x faster                                             |
| logging_format             | 3.98 us                                                | 3.44 us: 1.16x faster                                             |
| asyncio_tcp                | 449 ms                                                 | 390 ms: 1.15x faster                                              |
| coroutines                 | 19.2 ms                                                | 16.8 ms: 1.15x faster                                             |
| deepcopy_memo              | 27.7 us                                                | 24.2 us: 1.14x faster                                             |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 464 ms: 1.13x faster                                              |
| float                      | 55.8 ms                                                | 49.2 ms: 1.13x faster                                             |
| crypto_pyaes               | 51.9 ms                                                | 46.3 ms: 1.12x faster                                             |
| chaos                      | 42.5 ms                                                | 38.2 ms: 1.11x faster                                             |
| deepcopy                   | 235 us                                                 | 211 us: 1.11x faster                                              |
| mako                       | 7.71 ms                                                | 6.97 ms: 1.11x faster                                             |
| deepcopy_reduce            | 2.07 us                                                | 1.87 us: 1.11x faster                                             |
| pickle_pure_python         | 200 us                                                 | 182 us: 1.10x faster                                              |
| sqlglot_parse              | 848 us                                                 | 776 us: 1.09x faster                                              |
| tomli_loads                | 1.39 sec                                               | 1.28 sec: 1.09x faster                                            |
| deltablue                  | 2.71 ms                                                | 2.48 ms: 1.09x faster                                             |
| sqlglot_transpile          | 1.02 ms                                                | 943 us: 1.08x faster                                              |
| richards                   | 32.1 ms                                                | 29.7 ms: 1.08x faster                                             |
| unpickle_pure_python       | 151 us                                                 | 139 us: 1.08x faster                                              |
| richards_super             | 36.0 ms                                                | 33.3 ms: 1.08x faster                                             |
| xml_etree_process          | 39.7 ms                                                | 37.3 ms: 1.06x faster                                             |
| sqlglot_normalize          | 186 ms                                                 | 176 ms: 1.06x faster                                              |
| chameleon                  | 4.70 ms                                                | 4.47 ms: 1.05x faster                                             |
| json                       | 3.09 ms                                                | 2.94 ms: 1.05x faster                                             |
| scimark_monte_carlo        | 45.0 ms                                                | 43.0 ms: 1.05x faster                                             |
| pycparser                  | 677 ms                                                 | 652 ms: 1.04x faster                                              |
| spectral_norm              | 76.4 ms                                                | 73.7 ms: 1.04x faster                                             |
| nqueens                    | 62.4 ms                                                | 60.6 ms: 1.03x faster                                             |
| bench_thread_pool          | 504 us                                                 | 489 us: 1.03x faster                                              |
| xml_etree_generate         | 55.8 ms                                                | 54.3 ms: 1.03x faster                                             |
| dulwich_log                | 29.8 ms                                                | 29.0 ms: 1.03x faster                                             |
| async_generators           | 304 ms                                                 | 297 ms: 1.02x faster                                              |
| json_loads                 | 17.2 us                                                | 16.9 us: 1.02x faster                                             |
| xml_etree_iterparse        | 74.0 ms                                                | 72.6 ms: 1.02x faster                                             |
| sympy_expand               | 241 ms                                                 | 237 ms: 1.02x faster                                              |
| sympy_str                  | 148 ms                                                 | 145 ms: 1.02x faster                                              |
| regex_dna                  | 154 ms                                                 | 152 ms: 1.01x faster                                              |
| sympy_sum                  | 77.6 ms                                                | 76.6 ms: 1.01x faster                                             |
| sqlglot_optimize           | 34.0 ms                                                | 33.7 ms: 1.01x faster                                             |
| unpickle_list              | 3.02 us                                                | 3.00 us: 1.01x faster                                             |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.12 ms: 1.00x faster                                             |
| sympy_integrate            | 11.4 ms                                                | 11.3 ms: 1.00x faster                                             |
| regex_effbot               | 2.64 ms                                                | 2.63 ms: 1.00x faster                                             |
| asyncio_websockets         | 409 ms                                                 | 408 ms: 1.00x faster                                              |
| pprint_safe_repr           | 497 ms                                                 | 499 ms: 1.00x slower                                              |
| pyflate                    | 316 ms                                                 | 317 ms: 1.01x slower                                              |
| pickle_dict                | 18.1 us                                                | 18.2 us: 1.01x slower                                             |
| sqlite_synth               | 1.57 us                                                | 1.58 us: 1.01x slower                                             |
| 2to3                       | 169 ms                                                 | 171 ms: 1.01x slower                                              |
| unpickle                   | 9.12 us                                                | 9.28 us: 1.02x slower                                             |
| json_dumps                 | 6.22 ms                                                | 6.33 ms: 1.02x slower                                             |
| pathlib                    | 24.2 ms                                                | 24.7 ms: 1.02x slower                                             |
| gc_traversal               | 2.40 ms                                                | 2.45 ms: 1.02x slower                                             |
| scimark_fft                | 195 ms                                                 | 200 ms: 1.02x slower                                              |
| pickle_list                | 2.89 us                                                | 2.96 us: 1.03x slower                                             |
| bench_mp_pool              | 44.9 ms                                                | 46.1 ms: 1.03x slower                                             |
| nbody                      | 68.8 ms                                                | 70.7 ms: 1.03x slower                                             |
| docutils                   | 1.50 sec                                               | 1.55 sec: 1.03x slower                                            |
| meteor_contest             | 71.7 ms                                                | 74.2 ms: 1.03x slower                                             |
| pickle                     | 7.23 us                                                | 7.50 us: 1.04x slower                                             |
| aiohttp                    | 1.08 ms                                                | 1.12 ms: 1.04x slower                                             |
| go                         | 102 ms                                                 | 107 ms: 1.05x slower                                              |
| fannkuch                   | 248 ms                                                 | 263 ms: 1.06x slower                                              |
| hexiom                     | 4.54 ms                                                | 4.82 ms: 1.06x slower                                             |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.32 sec: 1.06x slower                                            |
| mypy2                      | 380 ms                                                 | 409 ms: 1.07x slower                                              |
| scimark_lu                 | 76.0 ms                                                | 81.7 ms: 1.08x slower                                             |
| regex_v8                   | 16.0 ms                                                | 17.2 ms: 1.08x slower                                             |
| regex_compile              | 77.9 ms                                                | 86.4 ms: 1.11x slower                                             |
| tornado_http               | 69.3 ms                                                | 80.2 ms: 1.16x slower                                             |
| python_startup             | 11.4 ms                                                | 13.3 ms: 1.16x slower                                             |
| coverage                   | 38.9 ms                                                | 46.3 ms: 1.19x slower                                             |
| scimark_sor                | 87.4 ms                                                | 106 ms: 1.21x slower                                              |
| telco                      | 3.68 ms                                                | 4.54 ms: 1.23x slower                                             |
| python_startup_no_site     | 9.37 ms                                                | 11.6 ms: 1.24x slower                                             |
| create_gc_cycles           | 701 us                                                 | 894 us: 1.27x slower                                              |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                      |

Benchmark hidden because not significant (6): xml_etree_parse, dask, mdp, pprint_pformat, pidigits, gunicorn
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240403-3.13.0a5+-dcee362-JIT/bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.08% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.24x