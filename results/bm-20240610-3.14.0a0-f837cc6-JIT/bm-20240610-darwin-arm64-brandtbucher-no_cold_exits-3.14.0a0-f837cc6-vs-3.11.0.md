# Results vs. 3.11.0

- fork: brandtbucher
- ref: no_cold_exits
- machine: darwin-arm64
- commit hash: f837cc6
- commit date: 2024-06-10
- overall geometric mean: 1.02x faster
- HPT reliability: 58.88%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.88x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 168 ms: 1.09x slower                                                 |
| docutils       | 1.43 sec                                               | 1.50 sec: 1.05x slower                                               |
| html5lib       | 33.0 ms                                                | 30.7 ms: 1.07x faster                                                |
| Geometric mean | (ref)                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 238 ms: 1.48x faster                                                 |
| async_tree_none_tg         | 276 ms                                                 | 196 ms: 1.41x faster                                                 |
| async_tree_none            | 282 ms                                                 | 214 ms: 1.31x faster                                                 |
| async_tree_io_tg           | 724 ms                                                 | 554 ms: 1.31x faster                                                 |
| async_tree_memoization     | 336 ms                                                 | 263 ms: 1.28x faster                                                 |
| async_tree_io              | 697 ms                                                 | 571 ms: 1.22x faster                                                 |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 451 ms: 1.22x faster                                                 |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 472 ms: 1.10x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.29x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 47.6 ms: 1.07x faster                                                |
| pidigits       | 280 ms                                                 | 282 ms: 1.00x slower                                                 |
| nbody          | 61.7 ms                                                | 63.7 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                 |
| regex_compile  | 72.8 ms                                                | 73.4 ms: 1.01x slower                                                |
| regex_effbot   | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                |
| regex_v8       | 15.1 ms                                                | 17.3 ms: 1.15x slower                                                |
| Geometric mean | (ref)                                                  | 1.05x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.31 ms: 1.19x faster                                                |
| unpickle_pure_python | 149 us                                                 | 132 us: 1.13x faster                                                 |
| pickle_pure_python   | 191 us                                                 | 173 us: 1.11x faster                                                 |
| tomli_loads          | 1.27 sec                                               | 1.26 sec: 1.01x faster                                               |
| xml_etree_parse      | 100 ms                                                 | 102 ms: 1.02x slower                                                 |
| xml_etree_iterparse  | 68.3 ms                                                | 70.1 ms: 1.03x slower                                                |
| pickle               | 6.98 us                                                | 7.45 us: 1.07x slower                                                |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.07x slower                                                |
| xml_etree_process    | 33.6 ms                                                | 35.9 ms: 1.07x slower                                                |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                                |
| pickle_list          | 2.70 us                                                | 2.98 us: 1.11x slower                                                |
| xml_etree_generate   | 45.8 ms                                                | 51.2 ms: 1.12x slower                                                |
| unpickle             | 8.29 us                                                | 9.31 us: 1.12x slower                                                |
| unpickle_list        | 2.69 us                                                | 3.07 us: 1.14x slower                                                |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 14.1 ms: 1.31x slower                                                |
| python_startup_no_site | 8.57 ms                                                | 11.6 ms: 1.35x slower                                                |
| Geometric mean         | (ref)                                                  | 1.33x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.36 ms: 1.25x faster                                                |
| django_template | 20.1 ms                                                | 21.4 ms: 1.06x slower                                                |
| genshi_text     | 14.4 ms                                                | 16.1 ms: 1.12x slower                                                |
| genshi_xml      | 28.5 ms                                                | 39.6 ms: 1.39x slower                                                |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 94.1 us: 3.20x faster                                                |
| asyncio_tcp                | 643 ms                                                 | 415 ms: 1.55x faster                                                 |
| async_tree_memoization_tg  | 352 ms                                                 | 238 ms: 1.48x faster                                                 |
| async_tree_none_tg         | 276 ms                                                 | 196 ms: 1.41x faster                                                 |
| pylint                     | 253 ms                                                 | 182 ms: 1.39x faster                                                 |
| async_tree_none            | 282 ms                                                 | 214 ms: 1.31x faster                                                 |
| async_tree_io_tg           | 724 ms                                                 | 554 ms: 1.31x faster                                                 |
| generators                 | 30.3 ms                                                | 23.3 ms: 1.30x faster                                                |
| async_tree_memoization     | 336 ms                                                 | 263 ms: 1.28x faster                                                 |
| raytrace                   | 206 ms                                                 | 165 ms: 1.25x faster                                                 |
| mako                       | 7.93 ms                                                | 6.36 ms: 1.25x faster                                                |
| async_tree_io              | 697 ms                                                 | 571 ms: 1.22x faster                                                 |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 451 ms: 1.22x faster                                                 |
| deepcopy_memo              | 25.7 us                                                | 21.2 us: 1.21x faster                                                |
| chaos                      | 47.4 ms                                                | 39.5 ms: 1.20x faster                                                |
| json_dumps                 | 7.53 ms                                                | 6.31 ms: 1.19x faster                                                |
| comprehensions             | 14.4 us                                                | 12.4 us: 1.16x faster                                                |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.23 sec: 1.13x faster                                               |
| unpickle_pure_python       | 149 us                                                 | 132 us: 1.13x faster                                                 |
| deltablue                  | 2.75 ms                                                | 2.46 ms: 1.12x faster                                                |
| sympy_sum                  | 80.2 ms                                                | 72.4 ms: 1.11x faster                                                |
| pickle_pure_python         | 191 us                                                 | 173 us: 1.11x faster                                                 |
| logging_simple             | 3.41 us                                                | 3.09 us: 1.10x faster                                                |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 472 ms: 1.10x faster                                                 |
| richards_super             | 37.3 ms                                                | 34.2 ms: 1.09x faster                                                |
| logging_format             | 3.67 us                                                | 3.39 us: 1.08x faster                                                |
| coroutines                 | 17.2 ms                                                | 15.8 ms: 1.08x faster                                                |
| html5lib                   | 33.0 ms                                                | 30.7 ms: 1.07x faster                                                |
| pathlib                    | 23.2 ms                                                | 21.6 ms: 1.07x faster                                                |
| logging_silent             | 66.5 ns                                                | 62.3 ns: 1.07x faster                                                |
| float                      | 50.8 ms                                                | 47.6 ms: 1.07x faster                                                |
| sqlglot_parse              | 890 us                                                 | 840 us: 1.06x faster                                                 |
| sympy_str                  | 144 ms                                                 | 138 ms: 1.04x faster                                                 |
| deepcopy                   | 215 us                                                 | 207 us: 1.04x faster                                                 |
| sqlglot_transpile          | 1.05 ms                                                | 1.01 ms: 1.04x faster                                                |
| mdp                        | 1.48 sec                                               | 1.44 sec: 1.03x faster                                               |
| sympy_integrate            | 11.3 ms                                                | 10.9 ms: 1.03x faster                                                |
| hexiom                     | 4.58 ms                                                | 4.44 ms: 1.03x faster                                                |
| go                         | 105 ms                                                 | 103 ms: 1.03x faster                                                 |
| richards                   | 31.1 ms                                                | 30.4 ms: 1.02x faster                                                |
| tomli_loads                | 1.27 sec                                               | 1.26 sec: 1.01x faster                                               |
| pidigits                   | 280 ms                                                 | 282 ms: 1.00x slower                                                 |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                 |
| pprint_pformat             | 979 ms                                                 | 986 ms: 1.01x slower                                                 |
| regex_compile              | 72.8 ms                                                | 73.4 ms: 1.01x slower                                                |
| pprint_safe_repr           | 478 ms                                                 | 483 ms: 1.01x slower                                                 |
| scimark_monte_carlo        | 43.5 ms                                                | 44.0 ms: 1.01x slower                                                |
| dask                       | 219 ms                                                 | 222 ms: 1.01x slower                                                 |
| nqueens                    | 55.9 ms                                                | 57.1 ms: 1.02x slower                                                |
| deepcopy_reduce            | 1.79 us                                                | 1.83 us: 1.02x slower                                                |
| xml_etree_parse            | 100 ms                                                 | 102 ms: 1.02x slower                                                 |
| spectral_norm              | 65.7 ms                                                | 67.2 ms: 1.02x slower                                                |
| pycparser                  | 659 ms                                                 | 676 ms: 1.03x slower                                                 |
| xml_etree_iterparse        | 68.3 ms                                                | 70.1 ms: 1.03x slower                                                |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                                |
| nbody                      | 61.7 ms                                                | 63.7 ms: 1.03x slower                                                |
| bench_thread_pool          | 465 us                                                 | 481 us: 1.03x slower                                                 |
| meteor_contest             | 71.1 ms                                                | 73.5 ms: 1.04x slower                                                |
| sympy_expand               | 229 ms                                                 | 237 ms: 1.04x slower                                                 |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.92 ms: 1.04x slower                                                |
| coverage                   | 43.9 ms                                                | 45.9 ms: 1.05x slower                                                |
| docutils                   | 1.43 sec                                               | 1.50 sec: 1.05x slower                                               |
| fannkuch                   | 240 ms                                                 | 251 ms: 1.05x slower                                                 |
| regex_effbot               | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                |
| django_template            | 20.1 ms                                                | 21.4 ms: 1.06x slower                                                |
| thrift                     | 410 us                                                 | 437 us: 1.07x slower                                                 |
| json                       | 2.75 ms                                                | 2.94 ms: 1.07x slower                                                |
| pickle                     | 6.98 us                                                | 7.45 us: 1.07x slower                                                |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.07x slower                                                |
| xml_etree_process          | 33.6 ms                                                | 35.9 ms: 1.07x slower                                                |
| scimark_fft                | 173 ms                                                 | 185 ms: 1.07x slower                                                 |
| 2to3                       | 154 ms                                                 | 168 ms: 1.09x slower                                                 |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                                |
| pickle_list                | 2.70 us                                                | 2.98 us: 1.11x slower                                                |
| crypto_pyaes               | 47.5 ms                                                | 52.8 ms: 1.11x slower                                                |
| genshi_text                | 14.4 ms                                                | 16.1 ms: 1.12x slower                                                |
| xml_etree_generate         | 45.8 ms                                                | 51.2 ms: 1.12x slower                                                |
| sqlglot_optimize           | 29.6 ms                                                | 33.2 ms: 1.12x slower                                                |
| unpickle                   | 8.29 us                                                | 9.31 us: 1.12x slower                                                |
| pyflate                    | 284 ms                                                 | 320 ms: 1.13x slower                                                 |
| unpickle_list              | 2.69 us                                                | 3.07 us: 1.14x slower                                                |
| regex_v8                   | 15.1 ms                                                | 17.3 ms: 1.15x slower                                                |
| bench_mp_pool              | 41.0 ms                                                | 48.0 ms: 1.17x slower                                                |
| scimark_lu                 | 67.7 ms                                                | 79.4 ms: 1.17x slower                                                |
| sqlite_synth               | 1.26 us                                                | 1.55 us: 1.24x slower                                                |
| create_gc_cycles           | 711 us                                                 | 895 us: 1.26x slower                                                 |
| scimark_sor                | 79.2 ms                                                | 101 ms: 1.27x slower                                                 |
| python_startup             | 10.8 ms                                                | 14.1 ms: 1.31x slower                                                |
| python_startup_no_site     | 8.57 ms                                                | 11.6 ms: 1.35x slower                                                |
| genshi_xml                 | 28.5 ms                                                | 39.6 ms: 1.39x slower                                                |
| telco                      | 3.17 ms                                                | 4.57 ms: 1.44x slower                                                |
| async_generators           | 192 ms                                                 | 287 ms: 1.49x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (2): tornado_http, asyncio_websockets
Ignored benchmarks (10) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
Ignored benchmarks (8) of results/bm-20240610-3.14.0a0-f837cc6-JIT/bm-20240610-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 58.88% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.88x