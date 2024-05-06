# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier_2_call
- machine: darwin-arm64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 161 ms: 1.05x faster                                                    |
| chameleon      | 4.70 ms                                                | 4.45 ms: 1.05x faster                                                   |
| docutils       | 1.50 sec                                               | 1.45 sec: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 266 ms                                                 | 202 ms: 1.31x faster                                                    |
| async_tree_none_tg         | 258 ms                                                 | 197 ms: 1.31x faster                                                    |
| async_tree_memoization_tg  | 323 ms                                                 | 261 ms: 1.24x faster                                                    |
| async_tree_io_tg           | 669 ms                                                 | 563 ms: 1.19x faster                                                    |
| async_tree_io              | 668 ms                                                 | 568 ms: 1.18x faster                                                    |
| async_tree_memoization     | 312 ms                                                 | 268 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 468 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 463 ms: 1.14x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 51.1 ms: 1.09x faster                                                   |
| nbody          | 68.8 ms                                                | 69.9 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 77.9 ms                                                | 69.1 ms: 1.13x faster                                                   |
| regex_dna      | 154 ms                                                 | 153 ms: 1.01x faster                                                    |
| regex_effbot   | 2.64 ms                                                | 2.62 ms: 1.01x faster                                                   |
| regex_v8       | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 180 us: 1.11x faster                                                    |
| unpickle_pure_python | 151 us                                                 | 141 us: 1.06x faster                                                    |
| xml_etree_process    | 39.7 ms                                                | 37.8 ms: 1.05x faster                                                   |
| xml_etree_generate   | 55.8 ms                                                | 54.5 ms: 1.03x faster                                                   |
| xml_etree_parse      | 106 ms                                                 | 104 ms: 1.02x faster                                                    |
| xml_etree_iterparse  | 74.0 ms                                                | 72.5 ms: 1.02x faster                                                   |
| json_loads           | 17.2 us                                                | 16.9 us: 1.02x faster                                                   |
| unpickle_list        | 3.02 us                                                | 2.98 us: 1.01x faster                                                   |
| json_dumps           | 6.22 ms                                                | 6.19 ms: 1.00x faster                                                   |
| pickle_dict          | 18.1 us                                                | 18.1 us: 1.00x slower                                                   |
| unpickle             | 9.12 us                                                | 9.28 us: 1.02x slower                                                   |
| pickle_list          | 2.89 us                                                | 2.96 us: 1.03x slower                                                   |
| pickle               | 7.23 us                                                | 7.48 us: 1.03x slower                                                   |
| tomli_loads          | 1.39 sec                                               | 1.51 sec: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 9.37 ms                                                | 10.2 ms: 1.09x slower                                                   |
| python_startup         | 11.4 ms                                                | 13.0 ms: 1.14x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.11x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 22.3 ms                                                | 20.1 ms: 1.11x faster                                                   |
| mako            | 7.71 ms                                                | 7.12 ms: 1.08x faster                                                   |
| Geometric mean  | (ref)                                                  | 1.10x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| comprehensions             | 14.5 us                                                | 10.5 us: 1.39x faster                                                   |
| raytrace                   | 212 ms                                                 | 155 ms: 1.37x faster                                                    |
| async_tree_none            | 266 ms                                                 | 202 ms: 1.31x faster                                                    |
| async_tree_none_tg         | 258 ms                                                 | 197 ms: 1.31x faster                                                    |
| async_tree_memoization_tg  | 323 ms                                                 | 261 ms: 1.24x faster                                                    |
| deltablue                  | 2.71 ms                                                | 2.19 ms: 1.24x faster                                                   |
| logging_silent             | 76.4 ns                                                | 62.3 ns: 1.23x faster                                                   |
| deepcopy_memo              | 27.7 us                                                | 23.2 us: 1.19x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 563 ms: 1.19x faster                                                    |
| async_tree_io              | 668 ms                                                 | 568 ms: 1.18x faster                                                    |
| chaos                      | 42.5 ms                                                | 36.4 ms: 1.17x faster                                                   |
| async_tree_memoization     | 312 ms                                                 | 268 ms: 1.16x faster                                                    |
| logging_simple             | 3.69 us                                                | 3.17 us: 1.16x faster                                                   |
| logging_format             | 3.98 us                                                | 3.46 us: 1.15x faster                                                   |
| coroutines                 | 19.2 ms                                                | 16.8 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 468 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 463 ms: 1.14x faster                                                    |
| sqlglot_parse              | 848 us                                                 | 747 us: 1.13x faster                                                    |
| sqlglot_transpile          | 1.02 ms                                                | 906 us: 1.13x faster                                                    |
| regex_compile              | 77.9 ms                                                | 69.1 ms: 1.13x faster                                                   |
| deepcopy                   | 235 us                                                 | 209 us: 1.12x faster                                                    |
| nqueens                    | 62.4 ms                                                | 55.9 ms: 1.12x faster                                                   |
| django_template            | 22.3 ms                                                | 20.1 ms: 1.11x faster                                                   |
| scimark_lu                 | 76.0 ms                                                | 68.4 ms: 1.11x faster                                                   |
| crypto_pyaes               | 51.9 ms                                                | 46.7 ms: 1.11x faster                                                   |
| pickle_pure_python         | 200 us                                                 | 180 us: 1.11x faster                                                    |
| sympy_str                  | 148 ms                                                 | 134 ms: 1.10x faster                                                    |
| sqlglot_normalize          | 186 ms                                                 | 169 ms: 1.10x faster                                                    |
| sympy_sum                  | 77.6 ms                                                | 70.7 ms: 1.10x faster                                                   |
| deepcopy_reduce            | 2.07 us                                                | 1.89 us: 1.10x faster                                                   |
| sympy_integrate            | 11.4 ms                                                | 10.4 ms: 1.09x faster                                                   |
| float                      | 55.8 ms                                                | 51.1 ms: 1.09x faster                                                   |
| asyncio_tcp                | 449 ms                                                 | 411 ms: 1.09x faster                                                    |
| mako                       | 7.71 ms                                                | 7.12 ms: 1.08x faster                                                   |
| dulwich_log                | 29.8 ms                                                | 27.6 ms: 1.08x faster                                                   |
| sqlglot_optimize           | 34.0 ms                                                | 31.6 ms: 1.08x faster                                                   |
| hexiom                     | 4.54 ms                                                | 4.22 ms: 1.08x faster                                                   |
| generators                 | 31.1 ms                                                | 28.9 ms: 1.07x faster                                                   |
| bench_thread_pool          | 504 us                                                 | 471 us: 1.07x faster                                                    |
| async_generators           | 304 ms                                                 | 285 ms: 1.07x faster                                                    |
| unpickle_pure_python       | 151 us                                                 | 141 us: 1.06x faster                                                    |
| pycparser                  | 677 ms                                                 | 637 ms: 1.06x faster                                                    |
| spectral_norm              | 76.4 ms                                                | 72.1 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 497 ms                                                 | 470 ms: 1.06x faster                                                    |
| pprint_pformat             | 1.01 sec                                               | 958 ms: 1.06x faster                                                    |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 2.97 ms: 1.05x faster                                                   |
| chameleon                  | 4.70 ms                                                | 4.45 ms: 1.05x faster                                                   |
| json                       | 3.09 ms                                                | 2.93 ms: 1.05x faster                                                   |
| 2to3                       | 169 ms                                                 | 161 ms: 1.05x faster                                                    |
| xml_etree_process          | 39.7 ms                                                | 37.8 ms: 1.05x faster                                                   |
| sympy_expand               | 241 ms                                                 | 231 ms: 1.05x faster                                                    |
| docutils                   | 1.50 sec                                               | 1.45 sec: 1.03x faster                                                  |
| richards_super             | 36.0 ms                                                | 34.8 ms: 1.03x faster                                                   |
| mdp                        | 1.58 sec                                               | 1.53 sec: 1.03x faster                                                  |
| bench_mp_pool              | 44.9 ms                                                | 43.5 ms: 1.03x faster                                                   |
| xml_etree_generate         | 55.8 ms                                                | 54.5 ms: 1.03x faster                                                   |
| xml_etree_parse            | 106 ms                                                 | 104 ms: 1.02x faster                                                    |
| xml_etree_iterparse        | 74.0 ms                                                | 72.5 ms: 1.02x faster                                                   |
| json_loads                 | 17.2 us                                                | 16.9 us: 1.02x faster                                                   |
| scimark_monte_carlo        | 45.0 ms                                                | 44.3 ms: 1.02x faster                                                   |
| unpickle_list              | 3.02 us                                                | 2.98 us: 1.01x faster                                                   |
| sqlite_synth               | 1.57 us                                                | 1.55 us: 1.01x faster                                                   |
| richards                   | 32.1 ms                                                | 31.8 ms: 1.01x faster                                                   |
| regex_dna                  | 154 ms                                                 | 153 ms: 1.01x faster                                                    |
| regex_effbot               | 2.64 ms                                                | 2.62 ms: 1.01x faster                                                   |
| pathlib                    | 24.2 ms                                                | 24.0 ms: 1.01x faster                                                   |
| meteor_contest             | 71.7 ms                                                | 71.3 ms: 1.01x faster                                                   |
| go                         | 102 ms                                                 | 101 ms: 1.01x faster                                                    |
| json_dumps                 | 6.22 ms                                                | 6.19 ms: 1.00x faster                                                   |
| asyncio_websockets         | 409 ms                                                 | 409 ms: 1.00x faster                                                    |
| pickle_dict                | 18.1 us                                                | 18.1 us: 1.00x slower                                                   |
| nbody                      | 68.8 ms                                                | 69.9 ms: 1.02x slower                                                   |
| unpickle                   | 9.12 us                                                | 9.28 us: 1.02x slower                                                   |
| gc_traversal               | 2.40 ms                                                | 2.44 ms: 1.02x slower                                                   |
| pyflate                    | 316 ms                                                 | 323 ms: 1.02x slower                                                    |
| pickle_list                | 2.89 us                                                | 2.96 us: 1.03x slower                                                   |
| fannkuch                   | 248 ms                                                 | 256 ms: 1.03x slower                                                    |
| pickle                     | 7.23 us                                                | 7.48 us: 1.03x slower                                                   |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.32 sec: 1.06x slower                                                  |
| python_startup_no_site     | 9.37 ms                                                | 10.2 ms: 1.09x slower                                                   |
| tomli_loads                | 1.39 sec                                               | 1.51 sec: 1.09x slower                                                  |
| regex_v8                   | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                   |
| scimark_sor                | 87.4 ms                                                | 98.5 ms: 1.13x slower                                                   |
| python_startup             | 11.4 ms                                                | 13.0 ms: 1.14x slower                                                   |
| coverage                   | 38.9 ms                                                | 46.2 ms: 1.19x slower                                                   |
| telco                      | 3.68 ms                                                | 4.46 ms: 1.21x slower                                                   |
| mypy2                      | 380 ms                                                 | 462 ms: 1.21x slower                                                    |
| create_gc_cycles           | 701 us                                                 | 895 us: 1.28x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                            |

Benchmark hidden because not significant (7): gunicorn, aiohttp, dask, pidigits, scimark_fft, typing_runtime_protocols, tornado_http
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240426-3.13.0a6+-65aa34a/bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.04x