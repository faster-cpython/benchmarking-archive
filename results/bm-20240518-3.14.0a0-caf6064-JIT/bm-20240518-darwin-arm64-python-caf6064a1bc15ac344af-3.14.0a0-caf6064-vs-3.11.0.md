# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: darwin-arm64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.01x faster
- HPT reliability: 52.33%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.75x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 192 ms: 1.25x slower                                                  |
| chameleon      | 4.30 ms                                                | 4.45 ms: 1.03x slower                                                 |
| docutils       | 1.43 sec                                               | 1.52 sec: 1.06x slower                                                |
| html5lib       | 33.0 ms                                                | 30.9 ms: 1.07x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 242 ms: 1.46x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 200 ms: 1.38x faster                                                  |
| async_tree_none            | 282 ms                                                 | 212 ms: 1.33x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 261 ms: 1.29x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 572 ms: 1.27x faster                                                  |
| async_tree_io              | 697 ms                                                 | 567 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 453 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 470 ms: 1.10x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 47.5 ms: 1.07x faster                                                 |
| pidigits       | 280 ms                                                 | 282 ms: 1.00x slower                                                  |
| nbody          | 61.7 ms                                                | 63.5 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 72.5 ms: 1.00x faster                                                 |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| regex_effbot   | 2.43 ms                                                | 2.58 ms: 1.06x slower                                                 |
| regex_v8       | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.10 ms: 1.24x faster                                                 |
| unpickle_pure_python | 149 us                                                 | 131 us: 1.14x faster                                                  |
| pickle_pure_python   | 191 us                                                 | 172 us: 1.11x faster                                                  |
| tomli_loads          | 1.27 sec                                               | 1.25 sec: 1.02x faster                                                |
| xml_etree_parse      | 100 ms                                                 | 102 ms: 1.02x slower                                                  |
| xml_etree_iterparse  | 68.3 ms                                                | 71.1 ms: 1.04x slower                                                 |
| xml_etree_process    | 33.6 ms                                                | 35.3 ms: 1.05x slower                                                 |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.07x slower                                                 |
| pickle               | 6.98 us                                                | 7.48 us: 1.07x slower                                                 |
| unpickle_list        | 2.69 us                                                | 2.89 us: 1.08x slower                                                 |
| pickle_list          | 2.70 us                                                | 2.92 us: 1.08x slower                                                 |
| xml_etree_generate   | 45.8 ms                                                | 50.8 ms: 1.11x slower                                                 |
| json_loads           | 15.3 us                                                | 17.1 us: 1.11x slower                                                 |
| unpickle             | 8.29 us                                                | 9.39 us: 1.13x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 15.3 ms: 1.42x slower                                                 |
| python_startup_no_site | 8.57 ms                                                | 12.8 ms: 1.50x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.38 ms: 1.24x faster                                                 |
| django_template | 20.1 ms                                                | 21.0 ms: 1.04x slower                                                 |
| genshi_text     | 14.4 ms                                                | 17.0 ms: 1.18x slower                                                 |
| genshi_xml      | 28.5 ms                                                | 40.4 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.09x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 92.5 us: 3.25x faster                                                 |
| asyncio_tcp                | 643 ms                                                 | 424 ms: 1.52x faster                                                  |
| async_tree_memoization_tg  | 352 ms                                                 | 242 ms: 1.46x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 200 ms: 1.38x faster                                                  |
| pylint                     | 253 ms                                                 | 183 ms: 1.38x faster                                                  |
| async_tree_none            | 282 ms                                                 | 212 ms: 1.33x faster                                                  |
| generators                 | 30.3 ms                                                | 23.2 ms: 1.31x faster                                                 |
| async_tree_memoization     | 336 ms                                                 | 261 ms: 1.29x faster                                                  |
| raytrace                   | 206 ms                                                 | 161 ms: 1.28x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 572 ms: 1.27x faster                                                  |
| mako                       | 7.93 ms                                                | 6.38 ms: 1.24x faster                                                 |
| json_dumps                 | 7.53 ms                                                | 6.10 ms: 1.24x faster                                                 |
| async_tree_io              | 697 ms                                                 | 567 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 453 ms: 1.21x faster                                                  |
| chaos                      | 47.4 ms                                                | 39.2 ms: 1.21x faster                                                 |
| deepcopy_memo              | 25.7 us                                                | 21.5 us: 1.20x faster                                                 |
| comprehensions             | 14.4 us                                                | 12.3 us: 1.17x faster                                                 |
| unpickle_pure_python       | 149 us                                                 | 131 us: 1.14x faster                                                  |
| logging_simple             | 3.41 us                                                | 3.03 us: 1.12x faster                                                 |
| pickle_pure_python         | 191 us                                                 | 172 us: 1.11x faster                                                  |
| deltablue                  | 2.75 ms                                                | 2.48 ms: 1.11x faster                                                 |
| logging_format             | 3.67 us                                                | 3.31 us: 1.11x faster                                                 |
| sympy_sum                  | 80.2 ms                                                | 72.3 ms: 1.11x faster                                                 |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 470 ms: 1.10x faster                                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.29 sec: 1.08x faster                                                |
| coroutines                 | 17.2 ms                                                | 15.9 ms: 1.08x faster                                                 |
| logging_silent             | 66.5 ns                                                | 62.1 ns: 1.07x faster                                                 |
| float                      | 50.8 ms                                                | 47.5 ms: 1.07x faster                                                 |
| sqlglot_parse              | 890 us                                                 | 833 us: 1.07x faster                                                  |
| html5lib                   | 33.0 ms                                                | 30.9 ms: 1.07x faster                                                 |
| deepcopy                   | 215 us                                                 | 204 us: 1.05x faster                                                  |
| sympy_str                  | 144 ms                                                 | 138 ms: 1.04x faster                                                  |
| sqlglot_transpile          | 1.05 ms                                                | 1.01 ms: 1.04x faster                                                 |
| sympy_integrate            | 11.3 ms                                                | 10.9 ms: 1.03x faster                                                 |
| hexiom                     | 4.58 ms                                                | 4.43 ms: 1.03x faster                                                 |
| richards_super             | 37.3 ms                                                | 36.2 ms: 1.03x faster                                                 |
| pprint_safe_repr           | 478 ms                                                 | 466 ms: 1.03x faster                                                  |
| pprint_pformat             | 979 ms                                                 | 955 ms: 1.02x faster                                                  |
| go                         | 105 ms                                                 | 103 ms: 1.02x faster                                                  |
| pathlib                    | 23.2 ms                                                | 22.7 ms: 1.02x faster                                                 |
| tomli_loads                | 1.27 sec                                               | 1.25 sec: 1.02x faster                                                |
| fannkuch                   | 240 ms                                                 | 235 ms: 1.02x faster                                                  |
| regex_compile              | 72.8 ms                                                | 72.5 ms: 1.00x faster                                                 |
| asyncio_websockets         | 408 ms                                                 | 409 ms: 1.00x slower                                                  |
| pidigits                   | 280 ms                                                 | 282 ms: 1.00x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.81 us: 1.01x slower                                                 |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| dask                       | 219 ms                                                 | 223 ms: 1.02x slower                                                  |
| xml_etree_parse            | 100 ms                                                 | 102 ms: 1.02x slower                                                  |
| scimark_monte_carlo        | 43.5 ms                                                | 44.3 ms: 1.02x slower                                                 |
| pycparser                  | 659 ms                                                 | 671 ms: 1.02x slower                                                  |
| meteor_contest             | 71.1 ms                                                | 72.5 ms: 1.02x slower                                                 |
| spectral_norm              | 65.7 ms                                                | 67.2 ms: 1.02x slower                                                 |
| nqueens                    | 55.9 ms                                                | 57.4 ms: 1.03x slower                                                 |
| nbody                      | 61.7 ms                                                | 63.5 ms: 1.03x slower                                                 |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.90 ms: 1.03x slower                                                 |
| chameleon                  | 4.30 ms                                                | 4.45 ms: 1.03x slower                                                 |
| sympy_expand               | 229 ms                                                 | 237 ms: 1.03x slower                                                  |
| bench_thread_pool          | 465 us                                                 | 482 us: 1.04x slower                                                  |
| richards                   | 31.1 ms                                                | 32.2 ms: 1.04x slower                                                 |
| xml_etree_iterparse        | 68.3 ms                                                | 71.1 ms: 1.04x slower                                                 |
| coverage                   | 43.9 ms                                                | 45.7 ms: 1.04x slower                                                 |
| django_template            | 20.1 ms                                                | 21.0 ms: 1.04x slower                                                 |
| xml_etree_process          | 33.6 ms                                                | 35.3 ms: 1.05x slower                                                 |
| thrift                     | 410 us                                                 | 434 us: 1.06x slower                                                  |
| docutils                   | 1.43 sec                                               | 1.52 sec: 1.06x slower                                                |
| regex_effbot               | 2.43 ms                                                | 2.58 ms: 1.06x slower                                                 |
| json                       | 2.75 ms                                                | 2.94 ms: 1.07x slower                                                 |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.07x slower                                                 |
| scimark_fft                | 173 ms                                                 | 184 ms: 1.07x slower                                                  |
| pickle                     | 6.98 us                                                | 7.48 us: 1.07x slower                                                 |
| unpickle_list              | 2.69 us                                                | 2.89 us: 1.08x slower                                                 |
| pickle_list                | 2.70 us                                                | 2.92 us: 1.08x slower                                                 |
| mdp                        | 1.48 sec                                               | 1.62 sec: 1.09x slower                                                |
| crypto_pyaes               | 47.5 ms                                                | 51.9 ms: 1.09x slower                                                 |
| gc_traversal               | 2.38 ms                                                | 2.61 ms: 1.09x slower                                                 |
| pyflate                    | 284 ms                                                 | 314 ms: 1.11x slower                                                  |
| xml_etree_generate         | 45.8 ms                                                | 50.8 ms: 1.11x slower                                                 |
| json_loads                 | 15.3 us                                                | 17.1 us: 1.11x slower                                                 |
| sqlglot_optimize           | 29.6 ms                                                | 33.0 ms: 1.11x slower                                                 |
| unpickle                   | 8.29 us                                                | 9.39 us: 1.13x slower                                                 |
| regex_v8                   | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                 |
| scimark_lu                 | 67.7 ms                                                | 78.6 ms: 1.16x slower                                                 |
| genshi_text                | 14.4 ms                                                | 17.0 ms: 1.18x slower                                                 |
| bench_mp_pool              | 41.0 ms                                                | 49.0 ms: 1.20x slower                                                 |
| 2to3                       | 154 ms                                                 | 192 ms: 1.25x slower                                                  |
| sqlite_synth               | 1.26 us                                                | 1.57 us: 1.25x slower                                                 |
| scimark_sor                | 79.2 ms                                                | 99.9 ms: 1.26x slower                                                 |
| create_gc_cycles           | 711 us                                                 | 920 us: 1.29x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 40.4 ms: 1.42x slower                                                 |
| python_startup             | 10.8 ms                                                | 15.3 ms: 1.42x slower                                                 |
| telco                      | 3.17 ms                                                | 4.65 ms: 1.47x slower                                                 |
| python_startup_no_site     | 8.57 ms                                                | 12.8 ms: 1.50x slower                                                 |
| flaskblogging              | 2.35 ms                                                | 3.53 ms: 1.50x slower                                                 |
| async_generators           | 192 ms                                                 | 294 ms: 1.53x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): tornado_http
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dulwich_log, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
Ignored benchmarks (8) of results/bm-20240518-3.14.0a0-caf6064-JIT/bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 52.33% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.75x