# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: darwin-arm64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 162 ms: 1.05x faster                                                           |
| chameleon      | 4.70 ms                                                | 4.62 ms: 1.02x faster                                                          |
| docutils       | 1.50 sec                                               | 1.48 sec: 1.02x faster                                                         |
| tornado_http   | 69.3 ms                                                | 78.4 ms: 1.13x slower                                                          |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 266 ms                                                 | 205 ms: 1.30x faster                                                           |
| async_tree_none_tg         | 258 ms                                                 | 200 ms: 1.29x faster                                                           |
| async_tree_memoization_tg  | 323 ms                                                 | 262 ms: 1.23x faster                                                           |
| async_tree_io_tg           | 669 ms                                                 | 571 ms: 1.17x faster                                                           |
| async_tree_io              | 668 ms                                                 | 576 ms: 1.16x faster                                                           |
| async_tree_memoization     | 312 ms                                                 | 273 ms: 1.14x faster                                                           |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 471 ms: 1.13x faster                                                           |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 467 ms: 1.13x faster                                                           |
| Geometric mean             | (ref)                                                  | 1.19x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 52.2 ms: 1.07x faster                                                          |
| nbody          | 68.8 ms                                                | 65.7 ms: 1.05x faster                                                          |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                   |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 77.9 ms                                                | 70.9 ms: 1.10x faster                                                          |
| regex_dna      | 154 ms                                                 | 150 ms: 1.03x faster                                                           |
| regex_effbot   | 2.64 ms                                                | 2.59 ms: 1.02x faster                                                          |
| regex_v8       | 16.0 ms                                                | 17.5 ms: 1.10x slower                                                          |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 74.0 ms                                                | 68.5 ms: 1.08x faster                                                          |
| xml_etree_parse      | 106 ms                                                 | 99.2 ms: 1.07x faster                                                          |
| pickle_pure_python   | 200 us                                                 | 188 us: 1.06x faster                                                           |
| unpickle_list        | 3.02 us                                                | 2.90 us: 1.04x faster                                                          |
| unpickle_pure_python | 151 us                                                 | 145 us: 1.04x faster                                                           |
| xml_etree_process    | 39.7 ms                                                | 38.4 ms: 1.03x faster                                                          |
| json_loads           | 17.2 us                                                | 17.0 us: 1.01x faster                                                          |
| xml_etree_generate   | 55.8 ms                                                | 55.1 ms: 1.01x faster                                                          |
| pickle_dict          | 18.1 us                                                | 18.3 us: 1.02x slower                                                          |
| pickle_list          | 2.89 us                                                | 2.95 us: 1.02x slower                                                          |
| pickle               | 7.23 us                                                | 7.39 us: 1.02x slower                                                          |
| unpickle             | 9.12 us                                                | 9.32 us: 1.02x slower                                                          |
| tomli_loads          | 1.39 sec                                               | 1.51 sec: 1.09x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                   |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 9.37 ms                                                | 9.15 ms: 1.02x faster                                                          |
| python_startup         | 11.4 ms                                                | 11.9 ms: 1.05x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.01x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| django_template | 22.3 ms                                                | 20.6 ms: 1.08x faster                                                          |
| mako            | 7.71 ms                                                | 7.32 ms: 1.05x faster                                                          |
| Geometric mean  | (ref)                                                  | 1.07x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| raytrace                   | 212 ms                                                 | 157 ms: 1.35x faster                                                           |
| typing_runtime_protocols   | 93.0 us                                                | 69.5 us: 1.34x faster                                                          |
| comprehensions             | 14.5 us                                                | 11.2 us: 1.30x faster                                                          |
| async_tree_none            | 266 ms                                                 | 205 ms: 1.30x faster                                                           |
| async_tree_none_tg         | 258 ms                                                 | 200 ms: 1.29x faster                                                           |
| async_tree_memoization_tg  | 323 ms                                                 | 262 ms: 1.23x faster                                                           |
| deltablue                  | 2.71 ms                                                | 2.28 ms: 1.19x faster                                                          |
| async_tree_io_tg           | 669 ms                                                 | 571 ms: 1.17x faster                                                           |
| async_tree_io              | 668 ms                                                 | 576 ms: 1.16x faster                                                           |
| chaos                      | 42.5 ms                                                | 36.9 ms: 1.15x faster                                                          |
| logging_silent             | 76.4 ns                                                | 66.4 ns: 1.15x faster                                                          |
| logging_simple             | 3.69 us                                                | 3.21 us: 1.15x faster                                                          |
| logging_format             | 3.98 us                                                | 3.48 us: 1.15x faster                                                          |
| async_tree_memoization     | 312 ms                                                 | 273 ms: 1.14x faster                                                           |
| generators                 | 31.1 ms                                                | 27.2 ms: 1.14x faster                                                          |
| deepcopy_memo              | 27.7 us                                                | 24.3 us: 1.14x faster                                                          |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 471 ms: 1.13x faster                                                           |
| nqueens                    | 62.4 ms                                                | 55.2 ms: 1.13x faster                                                          |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 467 ms: 1.13x faster                                                           |
| coroutines                 | 19.2 ms                                                | 17.4 ms: 1.10x faster                                                          |
| sqlglot_parse              | 848 us                                                 | 772 us: 1.10x faster                                                           |
| regex_compile              | 77.9 ms                                                | 70.9 ms: 1.10x faster                                                          |
| sqlglot_transpile          | 1.02 ms                                                | 932 us: 1.10x faster                                                           |
| crypto_pyaes               | 51.9 ms                                                | 47.4 ms: 1.10x faster                                                          |
| deepcopy                   | 235 us                                                 | 215 us: 1.09x faster                                                           |
| scimark_lu                 | 76.0 ms                                                | 69.6 ms: 1.09x faster                                                          |
| sympy_str                  | 148 ms                                                 | 136 ms: 1.09x faster                                                           |
| sympy_integrate            | 11.4 ms                                                | 10.5 ms: 1.08x faster                                                          |
| sympy_sum                  | 77.6 ms                                                | 71.7 ms: 1.08x faster                                                          |
| django_template            | 22.3 ms                                                | 20.6 ms: 1.08x faster                                                          |
| deepcopy_reduce            | 2.07 us                                                | 1.91 us: 1.08x faster                                                          |
| sqlglot_normalize          | 186 ms                                                 | 172 ms: 1.08x faster                                                           |
| xml_etree_iterparse        | 74.0 ms                                                | 68.5 ms: 1.08x faster                                                          |
| spectral_norm              | 76.4 ms                                                | 71.1 ms: 1.07x faster                                                          |
| xml_etree_parse            | 106 ms                                                 | 99.2 ms: 1.07x faster                                                          |
| float                      | 55.8 ms                                                | 52.2 ms: 1.07x faster                                                          |
| bench_thread_pool          | 504 us                                                 | 473 us: 1.07x faster                                                           |
| pickle_pure_python         | 200 us                                                 | 188 us: 1.06x faster                                                           |
| hexiom                     | 4.54 ms                                                | 4.27 ms: 1.06x faster                                                          |
| dulwich_log                | 29.8 ms                                                | 28.1 ms: 1.06x faster                                                          |
| sqlglot_optimize           | 34.0 ms                                                | 32.1 ms: 1.06x faster                                                          |
| json                       | 3.09 ms                                                | 2.92 ms: 1.06x faster                                                          |
| mako                       | 7.71 ms                                                | 7.32 ms: 1.05x faster                                                          |
| async_generators           | 304 ms                                                 | 290 ms: 1.05x faster                                                           |
| 2to3                       | 169 ms                                                 | 162 ms: 1.05x faster                                                           |
| nbody                      | 68.8 ms                                                | 65.7 ms: 1.05x faster                                                          |
| bench_mp_pool              | 44.9 ms                                                | 43.0 ms: 1.04x faster                                                          |
| sympy_expand               | 241 ms                                                 | 231 ms: 1.04x faster                                                           |
| unpickle_list              | 3.02 us                                                | 2.90 us: 1.04x faster                                                          |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.02 ms: 1.04x faster                                                          |
| unpickle_pure_python       | 151 us                                                 | 145 us: 1.04x faster                                                           |
| pycparser                  | 677 ms                                                 | 654 ms: 1.04x faster                                                           |
| xml_etree_process          | 39.7 ms                                                | 38.4 ms: 1.03x faster                                                          |
| regex_dna                  | 154 ms                                                 | 150 ms: 1.03x faster                                                           |
| mdp                        | 1.58 sec                                               | 1.54 sec: 1.03x faster                                                         |
| python_startup_no_site     | 9.37 ms                                                | 9.15 ms: 1.02x faster                                                          |
| pprint_pformat             | 1.01 sec                                               | 989 ms: 1.02x faster                                                           |
| pprint_safe_repr           | 497 ms                                                 | 487 ms: 1.02x faster                                                           |
| regex_effbot               | 2.64 ms                                                | 2.59 ms: 1.02x faster                                                          |
| pathlib                    | 24.2 ms                                                | 23.7 ms: 1.02x faster                                                          |
| docutils                   | 1.50 sec                                               | 1.48 sec: 1.02x faster                                                         |
| chameleon                  | 4.70 ms                                                | 4.62 ms: 1.02x faster                                                          |
| dask                       | 222 ms                                                 | 219 ms: 1.02x faster                                                           |
| json_loads                 | 17.2 us                                                | 17.0 us: 1.01x faster                                                          |
| xml_etree_generate         | 55.8 ms                                                | 55.1 ms: 1.01x faster                                                          |
| sqlite_synth               | 1.57 us                                                | 1.56 us: 1.01x faster                                                          |
| richards_super             | 36.0 ms                                                | 35.8 ms: 1.01x faster                                                          |
| scimark_monte_carlo        | 45.0 ms                                                | 44.8 ms: 1.00x faster                                                          |
| meteor_contest             | 71.7 ms                                                | 71.4 ms: 1.00x faster                                                          |
| asyncio_websockets         | 409 ms                                                 | 408 ms: 1.00x faster                                                           |
| go                         | 102 ms                                                 | 102 ms: 1.01x slower                                                           |
| richards                   | 32.1 ms                                                | 32.4 ms: 1.01x slower                                                          |
| pickle_dict                | 18.1 us                                                | 18.3 us: 1.02x slower                                                          |
| pickle_list                | 2.89 us                                                | 2.95 us: 1.02x slower                                                          |
| pickle                     | 7.23 us                                                | 7.39 us: 1.02x slower                                                          |
| unpickle                   | 9.12 us                                                | 9.32 us: 1.02x slower                                                          |
| gc_traversal               | 2.40 ms                                                | 2.46 ms: 1.02x slower                                                          |
| fannkuch                   | 248 ms                                                 | 257 ms: 1.03x slower                                                           |
| python_startup             | 11.4 ms                                                | 11.9 ms: 1.05x slower                                                          |
| pyflate                    | 316 ms                                                 | 330 ms: 1.05x slower                                                           |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.31 sec: 1.06x slower                                                         |
| tomli_loads                | 1.39 sec                                               | 1.51 sec: 1.09x slower                                                         |
| regex_v8                   | 16.0 ms                                                | 17.5 ms: 1.10x slower                                                          |
| tornado_http               | 69.3 ms                                                | 78.4 ms: 1.13x slower                                                          |
| scimark_sor                | 87.4 ms                                                | 100 ms: 1.14x slower                                                           |
| coverage                   | 38.9 ms                                                | 46.6 ms: 1.20x slower                                                          |
| telco                      | 3.68 ms                                                | 4.63 ms: 1.26x slower                                                          |
| create_gc_cycles           | 701 us                                                 | 897 us: 1.28x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                                   |

Benchmark hidden because not significant (7): asyncio_tcp, gunicorn, aiohttp, json_dumps, scimark_fft, pidigits, mypy2
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240422-3.13.0a6+-a6d4fd4/bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.05x