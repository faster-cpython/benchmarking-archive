# Results vs. 3.12.0

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: darwin-arm64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 162 ms: 1.04x faster                                                             |
| chameleon      | 4.70 ms                                                | 4.40 ms: 1.07x faster                                                            |
| docutils       | 1.50 sec                                               | 1.49 sec: 1.01x faster                                                           |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 258 ms                                                 | 196 ms: 1.32x faster                                                             |
| async_tree_none            | 266 ms                                                 | 202 ms: 1.31x faster                                                             |
| async_tree_memoization_tg  | 323 ms                                                 | 259 ms: 1.24x faster                                                             |
| async_tree_io_tg           | 669 ms                                                 | 558 ms: 1.20x faster                                                             |
| async_tree_memoization     | 312 ms                                                 | 260 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 452 ms: 1.18x faster                                                             |
| async_tree_io              | 668 ms                                                 | 567 ms: 1.18x faster                                                             |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 462 ms: 1.14x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 51.0 ms: 1.09x faster                                                            |
| nbody          | 68.8 ms                                                | 65.0 ms: 1.06x faster                                                            |
| Geometric mean | (ref)                                                  | 1.05x faster                                                                     |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 77.9 ms                                                | 70.2 ms: 1.11x faster                                                            |
| regex_dna      | 154 ms                                                 | 155 ms: 1.00x slower                                                             |
| regex_effbot   | 2.64 ms                                                | 2.72 ms: 1.03x slower                                                            |
| regex_v8       | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                            |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 183 us: 1.09x faster                                                             |
| xml_etree_iterparse  | 74.0 ms                                                | 68.8 ms: 1.08x faster                                                            |
| xml_etree_parse      | 106 ms                                                 | 99.6 ms: 1.07x faster                                                            |
| xml_etree_process    | 39.7 ms                                                | 37.4 ms: 1.06x faster                                                            |
| unpickle_pure_python | 151 us                                                 | 146 us: 1.03x faster                                                             |
| xml_etree_generate   | 55.8 ms                                                | 54.2 ms: 1.03x faster                                                            |
| json_loads           | 17.2 us                                                | 17.0 us: 1.01x faster                                                            |
| pickle_dict          | 18.1 us                                                | 18.1 us: 1.00x slower                                                            |
| json_dumps           | 6.22 ms                                                | 6.25 ms: 1.00x slower                                                            |
| unpickle             | 9.12 us                                                | 9.30 us: 1.02x slower                                                            |
| pickle_list          | 2.89 us                                                | 2.95 us: 1.02x slower                                                            |
| pickle               | 7.23 us                                                | 7.48 us: 1.03x slower                                                            |
| tomli_loads          | 1.39 sec                                               | 1.50 sec: 1.08x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 11.4 ms                                                | 12.0 ms: 1.05x slower                                                            |
| python_startup_no_site | 9.37 ms                                                | 10.3 ms: 1.10x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|-----------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako      | 7.71 ms                                                | 7.14 ms: 1.08x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| comprehensions             | 14.5 us                                                | 10.2 us: 1.42x faster                                                            |
| raytrace                   | 212 ms                                                 | 153 ms: 1.38x faster                                                             |
| typing_runtime_protocols   | 93.0 us                                                | 69.4 us: 1.34x faster                                                            |
| async_tree_none_tg         | 258 ms                                                 | 196 ms: 1.32x faster                                                             |
| async_tree_none            | 266 ms                                                 | 202 ms: 1.31x faster                                                             |
| async_tree_memoization_tg  | 323 ms                                                 | 259 ms: 1.24x faster                                                             |
| deltablue                  | 2.71 ms                                                | 2.20 ms: 1.23x faster                                                            |
| async_tree_io_tg           | 669 ms                                                 | 558 ms: 1.20x faster                                                             |
| async_tree_memoization     | 312 ms                                                 | 260 ms: 1.20x faster                                                             |
| logging_silent             | 76.4 ns                                                | 64.3 ns: 1.19x faster                                                            |
| chaos                      | 42.5 ms                                                | 35.9 ms: 1.18x faster                                                            |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 452 ms: 1.18x faster                                                             |
| async_tree_io              | 668 ms                                                 | 567 ms: 1.18x faster                                                             |
| logging_simple             | 3.69 us                                                | 3.16 us: 1.17x faster                                                            |
| deepcopy_memo              | 27.7 us                                                | 23.7 us: 1.17x faster                                                            |
| logging_format             | 3.98 us                                                | 3.42 us: 1.16x faster                                                            |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 462 ms: 1.14x faster                                                             |
| generators                 | 31.1 ms                                                | 27.4 ms: 1.14x faster                                                            |
| sqlglot_parse              | 848 us                                                 | 747 us: 1.13x faster                                                             |
| coroutines                 | 19.2 ms                                                | 17.0 ms: 1.13x faster                                                            |
| sqlglot_transpile          | 1.02 ms                                                | 907 us: 1.13x faster                                                             |
| deepcopy                   | 235 us                                                 | 209 us: 1.12x faster                                                             |
| crypto_pyaes               | 51.9 ms                                                | 46.3 ms: 1.12x faster                                                            |
| nqueens                    | 62.4 ms                                                | 56.0 ms: 1.12x faster                                                            |
| regex_compile              | 77.9 ms                                                | 70.2 ms: 1.11x faster                                                            |
| scimark_lu                 | 76.0 ms                                                | 68.5 ms: 1.11x faster                                                            |
| deepcopy_reduce            | 2.07 us                                                | 1.88 us: 1.10x faster                                                            |
| float                      | 55.8 ms                                                | 51.0 ms: 1.09x faster                                                            |
| sympy_sum                  | 77.6 ms                                                | 71.0 ms: 1.09x faster                                                            |
| pickle_pure_python         | 200 us                                                 | 183 us: 1.09x faster                                                             |
| sympy_str                  | 148 ms                                                 | 135 ms: 1.09x faster                                                             |
| sqlglot_normalize          | 186 ms                                                 | 171 ms: 1.09x faster                                                             |
| sympy_integrate            | 11.4 ms                                                | 10.5 ms: 1.09x faster                                                            |
| hexiom                     | 4.54 ms                                                | 4.20 ms: 1.08x faster                                                            |
| mako                       | 7.71 ms                                                | 7.14 ms: 1.08x faster                                                            |
| asyncio_tcp                | 449 ms                                                 | 416 ms: 1.08x faster                                                             |
| xml_etree_iterparse        | 74.0 ms                                                | 68.8 ms: 1.08x faster                                                            |
| spectral_norm              | 76.4 ms                                                | 71.2 ms: 1.07x faster                                                            |
| bench_thread_pool          | 504 us                                                 | 471 us: 1.07x faster                                                             |
| chameleon                  | 4.70 ms                                                | 4.40 ms: 1.07x faster                                                            |
| xml_etree_parse            | 106 ms                                                 | 99.6 ms: 1.07x faster                                                            |
| sqlglot_optimize           | 34.0 ms                                                | 31.9 ms: 1.07x faster                                                            |
| xml_etree_process          | 39.7 ms                                                | 37.4 ms: 1.06x faster                                                            |
| nbody                      | 68.8 ms                                                | 65.0 ms: 1.06x faster                                                            |
| async_generators           | 304 ms                                                 | 287 ms: 1.06x faster                                                             |
| dulwich_log                | 29.8 ms                                                | 28.2 ms: 1.06x faster                                                            |
| pycparser                  | 677 ms                                                 | 644 ms: 1.05x faster                                                             |
| sympy_expand               | 241 ms                                                 | 230 ms: 1.05x faster                                                             |
| richards                   | 32.1 ms                                                | 30.6 ms: 1.05x faster                                                            |
| bench_mp_pool              | 44.9 ms                                                | 42.8 ms: 1.05x faster                                                            |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.00 ms: 1.05x faster                                                            |
| json                       | 3.09 ms                                                | 2.95 ms: 1.05x faster                                                            |
| richards_super             | 36.0 ms                                                | 34.5 ms: 1.05x faster                                                            |
| 2to3                       | 169 ms                                                 | 162 ms: 1.04x faster                                                             |
| mdp                        | 1.58 sec                                               | 1.53 sec: 1.03x faster                                                           |
| unpickle_pure_python       | 151 us                                                 | 146 us: 1.03x faster                                                             |
| xml_etree_generate         | 55.8 ms                                                | 54.2 ms: 1.03x faster                                                            |
| pprint_pformat             | 1.01 sec                                               | 983 ms: 1.03x faster                                                             |
| pprint_safe_repr           | 497 ms                                                 | 483 ms: 1.03x faster                                                             |
| scimark_monte_carlo        | 45.0 ms                                                | 44.1 ms: 1.02x faster                                                            |
| dask                       | 222 ms                                                 | 219 ms: 1.02x faster                                                             |
| json_loads                 | 17.2 us                                                | 17.0 us: 1.01x faster                                                            |
| sqlite_synth               | 1.57 us                                                | 1.56 us: 1.01x faster                                                            |
| docutils                   | 1.50 sec                                               | 1.49 sec: 1.01x faster                                                           |
| go                         | 102 ms                                                 | 101 ms: 1.01x faster                                                             |
| asyncio_websockets         | 409 ms                                                 | 408 ms: 1.00x faster                                                             |
| pickle_dict                | 18.1 us                                                | 18.1 us: 1.00x slower                                                            |
| regex_dna                  | 154 ms                                                 | 155 ms: 1.00x slower                                                             |
| json_dumps                 | 6.22 ms                                                | 6.25 ms: 1.00x slower                                                            |
| gc_traversal               | 2.40 ms                                                | 2.44 ms: 1.02x slower                                                            |
| unpickle                   | 9.12 us                                                | 9.30 us: 1.02x slower                                                            |
| pickle_list                | 2.89 us                                                | 2.95 us: 1.02x slower                                                            |
| pathlib                    | 24.2 ms                                                | 24.8 ms: 1.02x slower                                                            |
| pyflate                    | 316 ms                                                 | 325 ms: 1.03x slower                                                             |
| regex_effbot               | 2.64 ms                                                | 2.72 ms: 1.03x slower                                                            |
| pickle                     | 7.23 us                                                | 7.48 us: 1.03x slower                                                            |
| fannkuch                   | 248 ms                                                 | 260 ms: 1.05x slower                                                             |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.31 sec: 1.05x slower                                                           |
| python_startup             | 11.4 ms                                                | 12.0 ms: 1.05x slower                                                            |
| tomli_loads                | 1.39 sec                                               | 1.50 sec: 1.08x slower                                                           |
| regex_v8                   | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                            |
| python_startup_no_site     | 9.37 ms                                                | 10.3 ms: 1.10x slower                                                            |
| scimark_sor                | 87.4 ms                                                | 99.2 ms: 1.14x slower                                                            |
| coverage                   | 38.9 ms                                                | 46.4 ms: 1.19x slower                                                            |
| create_gc_cycles           | 701 us                                                 | 885 us: 1.26x slower                                                             |
| telco                      | 3.68 ms                                                | 4.65 ms: 1.26x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                     |

Benchmark hidden because not significant (8): meteor_contest, scimark_fft, unpickle_list, pidigits, mypy2, gunicorn, aiohttp, tornado_http
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240408-3.13.0a5+-4675ce8/bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.04x