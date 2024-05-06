# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: darwin-arm64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.02x faster
- HPT reliability: 84.40%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 162 ms: 1.05x slower                                                           |
| chameleon      | 4.30 ms                                                | 4.62 ms: 1.07x slower                                                          |
| docutils       | 1.43 sec                                               | 1.48 sec: 1.03x slower                                                         |
| html5lib       | 33.0 ms                                                | 32.1 ms: 1.03x faster                                                          |
| tornado_http   | 69.1 ms                                                | 78.4 ms: 1.13x slower                                                          |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none_tg         | 276 ms                                                 | 200 ms: 1.38x faster                                                           |
| async_tree_none            | 282 ms                                                 | 205 ms: 1.37x faster                                                           |
| async_tree_memoization_tg  | 352 ms                                                 | 262 ms: 1.34x faster                                                           |
| async_tree_io_tg           | 724 ms                                                 | 571 ms: 1.27x faster                                                           |
| async_tree_memoization     | 336 ms                                                 | 273 ms: 1.23x faster                                                           |
| async_tree_io              | 697 ms                                                 | 576 ms: 1.21x faster                                                           |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 471 ms: 1.17x faster                                                           |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 467 ms: 1.11x faster                                                           |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                           |
| float          | 50.8 ms                                                | 52.2 ms: 1.03x slower                                                          |
| nbody          | 61.7 ms                                                | 65.7 ms: 1.07x slower                                                          |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 70.9 ms: 1.03x faster                                                          |
| regex_dna      | 148 ms                                                 | 150 ms: 1.01x slower                                                           |
| regex_effbot   | 2.43 ms                                                | 2.59 ms: 1.07x slower                                                          |
| regex_v8       | 15.1 ms                                                | 17.5 ms: 1.16x slower                                                          |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.22 ms: 1.21x faster                                                          |
| unpickle_pure_python | 149 us                                                 | 145 us: 1.02x faster                                                           |
| pickle_pure_python   | 191 us                                                 | 188 us: 1.02x faster                                                           |
| xml_etree_parse      | 100 ms                                                 | 99.2 ms: 1.01x faster                                                          |
| pickle               | 6.98 us                                                | 7.39 us: 1.06x slower                                                          |
| pickle_dict          | 17.1 us                                                | 18.3 us: 1.07x slower                                                          |
| unpickle_list        | 2.69 us                                                | 2.90 us: 1.08x slower                                                          |
| pickle_list          | 2.70 us                                                | 2.95 us: 1.09x slower                                                          |
| json_loads           | 15.3 us                                                | 17.0 us: 1.11x slower                                                          |
| unpickle             | 8.29 us                                                | 9.32 us: 1.12x slower                                                          |
| xml_etree_process    | 33.6 ms                                                | 38.4 ms: 1.14x slower                                                          |
| tomli_loads          | 1.27 sec                                               | 1.51 sec: 1.19x slower                                                         |
| xml_etree_generate   | 45.8 ms                                                | 55.1 ms: 1.20x slower                                                          |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                                   |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 8.57 ms                                                | 9.15 ms: 1.07x slower                                                          |
| python_startup         | 10.8 ms                                                | 11.9 ms: 1.11x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.09x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 7.32 ms: 1.08x faster                                                          |
| genshi_text     | 14.4 ms                                                | 14.6 ms: 1.02x slower                                                          |
| django_template | 20.1 ms                                                | 20.6 ms: 1.02x slower                                                          |
| genshi_xml      | 28.5 ms                                                | 31.5 ms: 1.11x slower                                                          |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 69.5 us: 4.33x faster                                                          |
| asyncio_tcp                | 643 ms                                                 | 430 ms: 1.50x faster                                                           |
| pylint                     | 253 ms                                                 | 171 ms: 1.47x faster                                                           |
| async_tree_none_tg         | 276 ms                                                 | 200 ms: 1.38x faster                                                           |
| async_tree_none            | 282 ms                                                 | 205 ms: 1.37x faster                                                           |
| async_tree_memoization_tg  | 352 ms                                                 | 262 ms: 1.34x faster                                                           |
| raytrace                   | 206 ms                                                 | 157 ms: 1.31x faster                                                           |
| comprehensions             | 14.4 us                                                | 11.2 us: 1.29x faster                                                          |
| chaos                      | 47.4 ms                                                | 36.9 ms: 1.28x faster                                                          |
| async_tree_io_tg           | 724 ms                                                 | 571 ms: 1.27x faster                                                           |
| async_tree_memoization     | 336 ms                                                 | 273 ms: 1.23x faster                                                           |
| json_dumps                 | 7.53 ms                                                | 6.22 ms: 1.21x faster                                                          |
| async_tree_io              | 697 ms                                                 | 576 ms: 1.21x faster                                                           |
| deltablue                  | 2.75 ms                                                | 2.28 ms: 1.20x faster                                                          |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 471 ms: 1.17x faster                                                           |
| sqlglot_parse              | 890 us                                                 | 772 us: 1.15x faster                                                           |
| sqlglot_transpile          | 1.05 ms                                                | 932 us: 1.13x faster                                                           |
| sympy_sum                  | 80.2 ms                                                | 71.7 ms: 1.12x faster                                                          |
| generators                 | 30.3 ms                                                | 27.2 ms: 1.11x faster                                                          |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 467 ms: 1.11x faster                                                           |
| mako                       | 7.93 ms                                                | 7.32 ms: 1.08x faster                                                          |
| sympy_integrate            | 11.3 ms                                                | 10.5 ms: 1.07x faster                                                          |
| hexiom                     | 4.58 ms                                                | 4.27 ms: 1.07x faster                                                          |
| logging_simple             | 3.41 us                                                | 3.21 us: 1.06x faster                                                          |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.31 sec: 1.06x faster                                                         |
| deepcopy_memo              | 25.7 us                                                | 24.3 us: 1.06x faster                                                          |
| sympy_str                  | 144 ms                                                 | 136 ms: 1.06x faster                                                           |
| logging_format             | 3.67 us                                                | 3.48 us: 1.06x faster                                                          |
| richards_super             | 37.3 ms                                                | 35.8 ms: 1.04x faster                                                          |
| go                         | 105 ms                                                 | 102 ms: 1.03x faster                                                           |
| html5lib                   | 33.0 ms                                                | 32.1 ms: 1.03x faster                                                          |
| regex_compile              | 72.8 ms                                                | 70.9 ms: 1.03x faster                                                          |
| unpickle_pure_python       | 149 us                                                 | 145 us: 1.02x faster                                                           |
| pickle_pure_python         | 191 us                                                 | 188 us: 1.02x faster                                                           |
| dulwich_log                | 28.6 ms                                                | 28.1 ms: 1.02x faster                                                          |
| nqueens                    | 55.9 ms                                                | 55.2 ms: 1.01x faster                                                          |
| xml_etree_parse            | 100 ms                                                 | 99.2 ms: 1.01x faster                                                          |
| deepcopy                   | 215 us                                                 | 215 us: 1.00x faster                                                           |
| crypto_pyaes               | 47.5 ms                                                | 47.4 ms: 1.00x faster                                                          |
| meteor_contest             | 71.1 ms                                                | 71.4 ms: 1.01x slower                                                          |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                           |
| sympy_expand               | 229 ms                                                 | 231 ms: 1.01x slower                                                           |
| regex_dna                  | 148 ms                                                 | 150 ms: 1.01x slower                                                           |
| pprint_pformat             | 979 ms                                                 | 989 ms: 1.01x slower                                                           |
| coroutines                 | 17.2 ms                                                | 17.4 ms: 1.01x slower                                                          |
| genshi_text                | 14.4 ms                                                | 14.6 ms: 1.02x slower                                                          |
| bench_thread_pool          | 465 us                                                 | 473 us: 1.02x slower                                                           |
| pprint_safe_repr           | 478 ms                                                 | 487 ms: 1.02x slower                                                           |
| pathlib                    | 23.2 ms                                                | 23.7 ms: 1.02x slower                                                          |
| django_template            | 20.1 ms                                                | 20.6 ms: 1.02x slower                                                          |
| scimark_lu                 | 67.7 ms                                                | 69.6 ms: 1.03x slower                                                          |
| float                      | 50.8 ms                                                | 52.2 ms: 1.03x slower                                                          |
| scimark_monte_carlo        | 43.5 ms                                                | 44.8 ms: 1.03x slower                                                          |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                                          |
| docutils                   | 1.43 sec                                               | 1.48 sec: 1.03x slower                                                         |
| mdp                        | 1.48 sec                                               | 1.54 sec: 1.03x slower                                                         |
| mypy2                      | 372 ms                                                 | 385 ms: 1.03x slower                                                           |
| richards                   | 31.1 ms                                                | 32.4 ms: 1.04x slower                                                          |
| aiohttp                    | 1.02 ms                                                | 1.07 ms: 1.05x slower                                                          |
| 2to3                       | 154 ms                                                 | 162 ms: 1.05x slower                                                           |
| bench_mp_pool              | 41.0 ms                                                | 43.0 ms: 1.05x slower                                                          |
| pickle                     | 6.98 us                                                | 7.39 us: 1.06x slower                                                          |
| coverage                   | 43.9 ms                                                | 46.6 ms: 1.06x slower                                                          |
| sqlglot_normalize          | 162 ms                                                 | 172 ms: 1.06x slower                                                           |
| json                       | 2.75 ms                                                | 2.92 ms: 1.06x slower                                                          |
| nbody                      | 61.7 ms                                                | 65.7 ms: 1.07x slower                                                          |
| regex_effbot               | 2.43 ms                                                | 2.59 ms: 1.07x slower                                                          |
| deepcopy_reduce            | 1.79 us                                                | 1.91 us: 1.07x slower                                                          |
| python_startup_no_site     | 8.57 ms                                                | 9.15 ms: 1.07x slower                                                          |
| fannkuch                   | 240 ms                                                 | 257 ms: 1.07x slower                                                           |
| pickle_dict                | 17.1 us                                                | 18.3 us: 1.07x slower                                                          |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.02 ms: 1.07x slower                                                          |
| chameleon                  | 4.30 ms                                                | 4.62 ms: 1.07x slower                                                          |
| unpickle_list              | 2.69 us                                                | 2.90 us: 1.08x slower                                                          |
| spectral_norm              | 65.7 ms                                                | 71.1 ms: 1.08x slower                                                          |
| thrift                     | 410 us                                                 | 444 us: 1.08x slower                                                           |
| sqlglot_optimize           | 29.6 ms                                                | 32.1 ms: 1.08x slower                                                          |
| pickle_list                | 2.70 us                                                | 2.95 us: 1.09x slower                                                          |
| genshi_xml                 | 28.5 ms                                                | 31.5 ms: 1.11x slower                                                          |
| json_loads                 | 15.3 us                                                | 17.0 us: 1.11x slower                                                          |
| python_startup             | 10.8 ms                                                | 11.9 ms: 1.11x slower                                                          |
| unpickle                   | 8.29 us                                                | 9.32 us: 1.12x slower                                                          |
| scimark_fft                | 173 ms                                                 | 195 ms: 1.13x slower                                                           |
| tornado_http               | 69.1 ms                                                | 78.4 ms: 1.13x slower                                                          |
| xml_etree_process          | 33.6 ms                                                | 38.4 ms: 1.14x slower                                                          |
| regex_v8                   | 15.1 ms                                                | 17.5 ms: 1.16x slower                                                          |
| pyflate                    | 284 ms                                                 | 330 ms: 1.17x slower                                                           |
| tomli_loads                | 1.27 sec                                               | 1.51 sec: 1.19x slower                                                         |
| xml_etree_generate         | 45.8 ms                                                | 55.1 ms: 1.20x slower                                                          |
| sqlite_synth               | 1.26 us                                                | 1.56 us: 1.24x slower                                                          |
| create_gc_cycles           | 711 us                                                 | 897 us: 1.26x slower                                                           |
| scimark_sor                | 79.2 ms                                                | 100 ms: 1.26x slower                                                           |
| telco                      | 3.17 ms                                                | 4.63 ms: 1.46x slower                                                          |
| async_generators           | 192 ms                                                 | 290 ms: 1.51x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                                   |

Benchmark hidden because not significant (6): pycparser, logging_silent, dask, asyncio_websockets, xml_etree_iterparse, gunicorn
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240422-3.13.0a6+-a6d4fd4/bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 84.40% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.08x