# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: darwin-arm64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.03x faster
- HPT reliability: 59.78%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 161 ms: 1.04x slower                                                   |
| chameleon      | 4.30 ms                                                | 4.49 ms: 1.04x slower                                                  |
| docutils       | 1.43 sec                                               | 1.45 sec: 1.02x slower                                                 |
| html5lib       | 33.0 ms                                                | 31.9 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 276 ms                                                 | 197 ms: 1.40x faster                                                   |
| async_tree_none            | 282 ms                                                 | 202 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 259 ms: 1.36x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 558 ms: 1.30x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 270 ms: 1.24x faster                                                   |
| async_tree_io              | 697 ms                                                 | 566 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 466 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 463 ms: 1.12x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| nbody          | 61.7 ms                                                | 65.2 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 69.4 ms: 1.05x faster                                                  |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.63 ms: 1.09x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.26 ms: 1.20x faster                                                  |
| pickle_pure_python   | 191 us                                                 | 183 us: 1.05x faster                                                   |
| unpickle_pure_python | 149 us                                                 | 143 us: 1.04x faster                                                   |
| xml_etree_parse      | 100 ms                                                 | 99.0 ms: 1.01x faster                                                  |
| xml_etree_iterparse  | 68.3 ms                                                | 68.8 ms: 1.01x slower                                                  |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.06x slower                                                  |
| pickle               | 6.98 us                                                | 7.44 us: 1.07x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.90 us: 1.08x slower                                                  |
| unpickle             | 8.29 us                                                | 9.21 us: 1.11x slower                                                  |
| json_loads           | 15.3 us                                                | 17.1 us: 1.11x slower                                                  |
| pickle_list          | 2.70 us                                                | 3.01 us: 1.12x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 37.9 ms: 1.13x slower                                                  |
| tomli_loads          | 1.27 sec                                               | 1.50 sec: 1.18x slower                                                 |
| xml_etree_generate   | 45.8 ms                                                | 54.9 ms: 1.20x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 8.57 ms                                                | 9.12 ms: 1.06x slower                                                  |
| python_startup         | 10.8 ms                                                | 11.9 ms: 1.11x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 7.93 ms                                                | 7.14 ms: 1.11x faster                                                  |
| genshi_text    | 14.4 ms                                                | 14.7 ms: 1.02x slower                                                  |
| genshi_xml     | 28.5 ms                                                | 31.7 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 68.0 us: 4.43x faster                                                  |
| asyncio_tcp                | 643 ms                                                 | 406 ms: 1.59x faster                                                   |
| pylint                     | 253 ms                                                 | 170 ms: 1.49x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 197 ms: 1.40x faster                                                   |
| async_tree_none            | 282 ms                                                 | 202 ms: 1.39x faster                                                   |
| comprehensions             | 14.4 us                                                | 10.6 us: 1.37x faster                                                  |
| async_tree_memoization_tg  | 352 ms                                                 | 259 ms: 1.36x faster                                                   |
| raytrace                   | 206 ms                                                 | 153 ms: 1.35x faster                                                   |
| chaos                      | 47.4 ms                                                | 36.3 ms: 1.31x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 558 ms: 1.30x faster                                                   |
| deltablue                  | 2.75 ms                                                | 2.18 ms: 1.26x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 270 ms: 1.24x faster                                                   |
| async_tree_io              | 697 ms                                                 | 566 ms: 1.23x faster                                                   |
| json_dumps                 | 7.53 ms                                                | 6.26 ms: 1.20x faster                                                  |
| sqlglot_parse              | 890 us                                                 | 749 us: 1.19x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 466 ms: 1.18x faster                                                   |
| sqlglot_transpile          | 1.05 ms                                                | 908 us: 1.16x faster                                                   |
| sympy_sum                  | 80.2 ms                                                | 70.6 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 463 ms: 1.12x faster                                                   |
| mako                       | 7.93 ms                                                | 7.14 ms: 1.11x faster                                                  |
| richards_super             | 37.3 ms                                                | 34.3 ms: 1.09x faster                                                  |
| logging_simple             | 3.41 us                                                | 3.15 us: 1.08x faster                                                  |
| sympy_integrate            | 11.3 ms                                                | 10.4 ms: 1.08x faster                                                  |
| hexiom                     | 4.58 ms                                                | 4.24 ms: 1.08x faster                                                  |
| deepcopy_memo              | 25.7 us                                                | 23.9 us: 1.08x faster                                                  |
| sympy_str                  | 144 ms                                                 | 134 ms: 1.08x faster                                                   |
| logging_format             | 3.67 us                                                | 3.42 us: 1.07x faster                                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.32 sec: 1.06x faster                                                 |
| go                         | 105 ms                                                 | 100 ms: 1.05x faster                                                   |
| generators                 | 30.3 ms                                                | 28.9 ms: 1.05x faster                                                  |
| regex_compile              | 72.8 ms                                                | 69.4 ms: 1.05x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 183 us: 1.05x faster                                                   |
| unpickle_pure_python       | 149 us                                                 | 143 us: 1.04x faster                                                   |
| dulwich_log                | 28.6 ms                                                | 27.7 ms: 1.03x faster                                                  |
| html5lib                   | 33.0 ms                                                | 31.9 ms: 1.03x faster                                                  |
| pycparser                  | 659 ms                                                 | 640 ms: 1.03x faster                                                   |
| logging_silent             | 66.5 ns                                                | 64.8 ns: 1.03x faster                                                  |
| crypto_pyaes               | 47.5 ms                                                | 46.5 ms: 1.02x faster                                                  |
| xml_etree_parse            | 100 ms                                                 | 99.0 ms: 1.01x faster                                                  |
| pprint_pformat             | 979 ms                                                 | 972 ms: 1.01x faster                                                   |
| richards                   | 31.1 ms                                                | 31.2 ms: 1.00x slower                                                  |
| nqueens                    | 55.9 ms                                                | 56.3 ms: 1.01x slower                                                  |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                   |
| pidigits                   | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| xml_etree_iterparse        | 68.3 ms                                                | 68.8 ms: 1.01x slower                                                  |
| meteor_contest             | 71.1 ms                                                | 71.8 ms: 1.01x slower                                                  |
| bench_thread_pool          | 465 us                                                 | 472 us: 1.02x slower                                                   |
| docutils                   | 1.43 sec                                               | 1.45 sec: 1.02x slower                                                 |
| scimark_lu                 | 67.7 ms                                                | 68.9 ms: 1.02x slower                                                  |
| genshi_text                | 14.4 ms                                                | 14.7 ms: 1.02x slower                                                  |
| mypy2                      | 372 ms                                                 | 380 ms: 1.02x slower                                                   |
| scimark_monte_carlo        | 43.5 ms                                                | 44.5 ms: 1.02x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.44 ms: 1.03x slower                                                  |
| pathlib                    | 23.2 ms                                                | 24.0 ms: 1.03x slower                                                  |
| mdp                        | 1.48 sec                                               | 1.54 sec: 1.03x slower                                                 |
| 2to3                       | 154 ms                                                 | 161 ms: 1.04x slower                                                   |
| chameleon                  | 4.30 ms                                                | 4.49 ms: 1.04x slower                                                  |
| sqlglot_normalize          | 162 ms                                                 | 169 ms: 1.05x slower                                                   |
| aiohttp                    | 1.02 ms                                                | 1.07 ms: 1.05x slower                                                  |
| bench_mp_pool              | 41.0 ms                                                | 43.1 ms: 1.05x slower                                                  |
| nbody                      | 61.7 ms                                                | 65.2 ms: 1.06x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.90 us: 1.06x slower                                                  |
| python_startup_no_site     | 8.57 ms                                                | 9.12 ms: 1.06x slower                                                  |
| sqlglot_optimize           | 29.6 ms                                                | 31.5 ms: 1.06x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.06x slower                                                  |
| pickle                     | 6.98 us                                                | 7.44 us: 1.07x slower                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.02 ms: 1.07x slower                                                  |
| coverage                   | 43.9 ms                                                | 47.1 ms: 1.07x slower                                                  |
| json                       | 2.75 ms                                                | 2.96 ms: 1.07x slower                                                  |
| fannkuch                   | 240 ms                                                 | 258 ms: 1.08x slower                                                   |
| unpickle_list              | 2.69 us                                                | 2.90 us: 1.08x slower                                                  |
| spectral_norm              | 65.7 ms                                                | 71.0 ms: 1.08x slower                                                  |
| thrift                     | 410 us                                                 | 444 us: 1.08x slower                                                   |
| regex_effbot               | 2.43 ms                                                | 2.63 ms: 1.09x slower                                                  |
| python_startup             | 10.8 ms                                                | 11.9 ms: 1.11x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.21 us: 1.11x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 31.7 ms: 1.11x slower                                                  |
| json_loads                 | 15.3 us                                                | 17.1 us: 1.11x slower                                                  |
| pickle_list                | 2.70 us                                                | 3.01 us: 1.12x slower                                                  |
| scimark_fft                | 173 ms                                                 | 195 ms: 1.13x slower                                                   |
| xml_etree_process          | 33.6 ms                                                | 37.9 ms: 1.13x slower                                                  |
| pyflate                    | 284 ms                                                 | 322 ms: 1.14x slower                                                   |
| regex_v8                   | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                  |
| tomli_loads                | 1.27 sec                                               | 1.50 sec: 1.18x slower                                                 |
| xml_etree_generate         | 45.8 ms                                                | 54.9 ms: 1.20x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 872 us: 1.23x slower                                                   |
| sqlite_synth               | 1.26 us                                                | 1.56 us: 1.24x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 99.4 ms: 1.25x slower                                                  |
| telco                      | 3.17 ms                                                | 4.65 ms: 1.47x slower                                                  |
| async_generators           | 192 ms                                                 | 286 ms: 1.49x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (10): django_template, asyncio_websockets, dask, float, sympy_expand, deepcopy, pprint_safe_repr, coroutines, gunicorn, tornado_http
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 59.78% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.08x