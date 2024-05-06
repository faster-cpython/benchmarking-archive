# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier_2_call
- machine: darwin-arm64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.02x faster
- HPT reliability: 65.88%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 161 ms: 1.04x slower                                                    |
| chameleon      | 4.30 ms                                                | 4.45 ms: 1.04x slower                                                   |
| docutils       | 1.43 sec                                               | 1.45 sec: 1.01x slower                                                  |
| html5lib       | 33.0 ms                                                | 31.7 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                            |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 276 ms                                                 | 197 ms: 1.40x faster                                                    |
| async_tree_none            | 282 ms                                                 | 202 ms: 1.39x faster                                                    |
| async_tree_memoization_tg  | 352 ms                                                 | 261 ms: 1.35x faster                                                    |
| async_tree_io_tg           | 724 ms                                                 | 563 ms: 1.29x faster                                                    |
| async_tree_memoization     | 336 ms                                                 | 268 ms: 1.25x faster                                                    |
| async_tree_io              | 697 ms                                                 | 568 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 468 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 463 ms: 1.12x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 282 ms: 1.00x slower                                                    |
| float          | 50.8 ms                                                | 51.1 ms: 1.01x slower                                                   |
| nbody          | 61.7 ms                                                | 69.9 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 69.1 ms: 1.05x faster                                                   |
| regex_dna      | 148 ms                                                 | 153 ms: 1.03x slower                                                    |
| regex_effbot   | 2.43 ms                                                | 2.62 ms: 1.08x slower                                                   |
| regex_v8       | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.19 ms: 1.22x faster                                                   |
| pickle_pure_python   | 191 us                                                 | 180 us: 1.06x faster                                                    |
| unpickle_pure_python | 149 us                                                 | 141 us: 1.05x faster                                                    |
| xml_etree_parse      | 100 ms                                                 | 104 ms: 1.04x slower                                                    |
| pickle_dict          | 17.1 us                                                | 18.1 us: 1.06x slower                                                   |
| xml_etree_iterparse  | 68.3 ms                                                | 72.5 ms: 1.06x slower                                                   |
| pickle               | 6.98 us                                                | 7.48 us: 1.07x slower                                                   |
| pickle_list          | 2.70 us                                                | 2.96 us: 1.10x slower                                                   |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                                   |
| unpickle_list        | 2.69 us                                                | 2.98 us: 1.11x slower                                                   |
| unpickle             | 8.29 us                                                | 9.28 us: 1.12x slower                                                   |
| xml_etree_process    | 33.6 ms                                                | 37.8 ms: 1.13x slower                                                   |
| tomli_loads          | 1.27 sec                                               | 1.51 sec: 1.19x slower                                                  |
| xml_etree_generate   | 45.8 ms                                                | 54.5 ms: 1.19x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 8.57 ms                                                | 10.2 ms: 1.19x slower                                                   |
| python_startup         | 10.8 ms                                                | 13.0 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 7.12 ms: 1.11x faster                                                   |
| django_template | 20.1 ms                                                | 20.1 ms: 1.00x faster                                                   |
| genshi_text     | 14.4 ms                                                | 14.5 ms: 1.01x slower                                                   |
| genshi_xml      | 28.5 ms                                                | 31.5 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.00x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 93.1 us: 3.23x faster                                                   |
| asyncio_tcp                | 643 ms                                                 | 411 ms: 1.56x faster                                                    |
| pylint                     | 253 ms                                                 | 172 ms: 1.47x faster                                                    |
| async_tree_none_tg         | 276 ms                                                 | 197 ms: 1.40x faster                                                    |
| async_tree_none            | 282 ms                                                 | 202 ms: 1.39x faster                                                    |
| comprehensions             | 14.4 us                                                | 10.5 us: 1.38x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 261 ms: 1.35x faster                                                    |
| raytrace                   | 206 ms                                                 | 155 ms: 1.33x faster                                                    |
| chaos                      | 47.4 ms                                                | 36.4 ms: 1.30x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 563 ms: 1.29x faster                                                    |
| deltablue                  | 2.75 ms                                                | 2.19 ms: 1.26x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 268 ms: 1.25x faster                                                    |
| async_tree_io              | 697 ms                                                 | 568 ms: 1.23x faster                                                    |
| json_dumps                 | 7.53 ms                                                | 6.19 ms: 1.22x faster                                                   |
| sqlglot_parse              | 890 us                                                 | 747 us: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 468 ms: 1.17x faster                                                    |
| sqlglot_transpile          | 1.05 ms                                                | 906 us: 1.16x faster                                                    |
| sympy_sum                  | 80.2 ms                                                | 70.7 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 463 ms: 1.12x faster                                                    |
| mako                       | 7.93 ms                                                | 7.12 ms: 1.11x faster                                                   |
| deepcopy_memo              | 25.7 us                                                | 23.2 us: 1.11x faster                                                   |
| hexiom                     | 4.58 ms                                                | 4.22 ms: 1.08x faster                                                   |
| sympy_integrate            | 11.3 ms                                                | 10.4 ms: 1.08x faster                                                   |
| logging_simple             | 3.41 us                                                | 3.17 us: 1.08x faster                                                   |
| sympy_str                  | 144 ms                                                 | 134 ms: 1.07x faster                                                    |
| richards_super             | 37.3 ms                                                | 34.8 ms: 1.07x faster                                                   |
| logging_silent             | 66.5 ns                                                | 62.3 ns: 1.07x faster                                                   |
| logging_format             | 3.67 us                                                | 3.46 us: 1.06x faster                                                   |
| pickle_pure_python         | 191 us                                                 | 180 us: 1.06x faster                                                    |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.32 sec: 1.06x faster                                                  |
| regex_compile              | 72.8 ms                                                | 69.1 ms: 1.05x faster                                                   |
| unpickle_pure_python       | 149 us                                                 | 141 us: 1.05x faster                                                    |
| generators                 | 30.3 ms                                                | 28.9 ms: 1.05x faster                                                   |
| go                         | 105 ms                                                 | 101 ms: 1.04x faster                                                    |
| html5lib                   | 33.0 ms                                                | 31.7 ms: 1.04x faster                                                   |
| dulwich_log                | 28.6 ms                                                | 27.6 ms: 1.04x faster                                                   |
| pycparser                  | 659 ms                                                 | 637 ms: 1.03x faster                                                    |
| deepcopy                   | 215 us                                                 | 209 us: 1.03x faster                                                    |
| coroutines                 | 17.2 ms                                                | 16.8 ms: 1.02x faster                                                   |
| pprint_pformat             | 979 ms                                                 | 958 ms: 1.02x faster                                                    |
| pprint_safe_repr           | 478 ms                                                 | 470 ms: 1.02x faster                                                    |
| crypto_pyaes               | 47.5 ms                                                | 46.7 ms: 1.02x faster                                                   |
| django_template            | 20.1 ms                                                | 20.1 ms: 1.00x faster                                                   |
| meteor_contest             | 71.1 ms                                                | 71.3 ms: 1.00x slower                                                   |
| pidigits                   | 280 ms                                                 | 282 ms: 1.00x slower                                                    |
| float                      | 50.8 ms                                                | 51.1 ms: 1.01x slower                                                   |
| sympy_expand               | 229 ms                                                 | 231 ms: 1.01x slower                                                    |
| scimark_lu                 | 67.7 ms                                                | 68.4 ms: 1.01x slower                                                   |
| genshi_text                | 14.4 ms                                                | 14.5 ms: 1.01x slower                                                   |
| bench_thread_pool          | 465 us                                                 | 471 us: 1.01x slower                                                    |
| docutils                   | 1.43 sec                                               | 1.45 sec: 1.01x slower                                                  |
| scimark_monte_carlo        | 43.5 ms                                                | 44.3 ms: 1.02x slower                                                   |
| richards                   | 31.1 ms                                                | 31.8 ms: 1.02x slower                                                   |
| gc_traversal               | 2.38 ms                                                | 2.44 ms: 1.03x slower                                                   |
| mdp                        | 1.48 sec                                               | 1.53 sec: 1.03x slower                                                  |
| aiohttp                    | 1.02 ms                                                | 1.06 ms: 1.03x slower                                                   |
| regex_dna                  | 148 ms                                                 | 153 ms: 1.03x slower                                                    |
| pathlib                    | 23.2 ms                                                | 24.0 ms: 1.04x slower                                                   |
| chameleon                  | 4.30 ms                                                | 4.45 ms: 1.04x slower                                                   |
| xml_etree_parse            | 100 ms                                                 | 104 ms: 1.04x slower                                                    |
| 2to3                       | 154 ms                                                 | 161 ms: 1.04x slower                                                    |
| sqlglot_normalize          | 162 ms                                                 | 169 ms: 1.04x slower                                                    |
| deepcopy_reduce            | 1.79 us                                                | 1.89 us: 1.05x slower                                                   |
| coverage                   | 43.9 ms                                                | 46.2 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.97 ms: 1.06x slower                                                   |
| bench_mp_pool              | 41.0 ms                                                | 43.5 ms: 1.06x slower                                                   |
| pickle_dict                | 17.1 us                                                | 18.1 us: 1.06x slower                                                   |
| xml_etree_iterparse        | 68.3 ms                                                | 72.5 ms: 1.06x slower                                                   |
| json                       | 2.75 ms                                                | 2.93 ms: 1.06x slower                                                   |
| sqlglot_optimize           | 29.6 ms                                                | 31.6 ms: 1.06x slower                                                   |
| fannkuch                   | 240 ms                                                 | 256 ms: 1.07x slower                                                    |
| pickle                     | 6.98 us                                                | 7.48 us: 1.07x slower                                                   |
| regex_effbot               | 2.43 ms                                                | 2.62 ms: 1.08x slower                                                   |
| thrift                     | 410 us                                                 | 448 us: 1.09x slower                                                    |
| spectral_norm              | 65.7 ms                                                | 72.1 ms: 1.10x slower                                                   |
| pickle_list                | 2.70 us                                                | 2.96 us: 1.10x slower                                                   |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                                   |
| genshi_xml                 | 28.5 ms                                                | 31.5 ms: 1.11x slower                                                   |
| unpickle_list              | 2.69 us                                                | 2.98 us: 1.11x slower                                                   |
| unpickle                   | 8.29 us                                                | 9.28 us: 1.12x slower                                                   |
| xml_etree_process          | 33.6 ms                                                | 37.8 ms: 1.13x slower                                                   |
| scimark_fft                | 173 ms                                                 | 195 ms: 1.13x slower                                                    |
| nbody                      | 61.7 ms                                                | 69.9 ms: 1.13x slower                                                   |
| pyflate                    | 284 ms                                                 | 323 ms: 1.14x slower                                                    |
| regex_v8                   | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                   |
| python_startup_no_site     | 8.57 ms                                                | 10.2 ms: 1.19x slower                                                   |
| tomli_loads                | 1.27 sec                                               | 1.51 sec: 1.19x slower                                                  |
| xml_etree_generate         | 45.8 ms                                                | 54.5 ms: 1.19x slower                                                   |
| python_startup             | 10.8 ms                                                | 13.0 ms: 1.21x slower                                                   |
| sqlite_synth               | 1.26 us                                                | 1.55 us: 1.24x slower                                                   |
| mypy2                      | 372 ms                                                 | 462 ms: 1.24x slower                                                    |
| scimark_sor                | 79.2 ms                                                | 98.5 ms: 1.24x slower                                                   |
| create_gc_cycles           | 711 us                                                 | 895 us: 1.26x slower                                                    |
| telco                      | 3.17 ms                                                | 4.46 ms: 1.41x slower                                                   |
| async_generators           | 192 ms                                                 | 285 ms: 1.49x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (5): nqueens, asyncio_websockets, gunicorn, dask, tornado_http
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240426-3.13.0a6+-65aa34a/bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 65.88% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x