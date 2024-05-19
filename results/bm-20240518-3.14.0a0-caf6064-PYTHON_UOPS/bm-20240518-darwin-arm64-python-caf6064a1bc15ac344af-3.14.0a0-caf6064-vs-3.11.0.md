# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: darwin-arm64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.10x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 0.49x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 182 ms: 1.18x slower                                                  |
| chameleon      | 4.30 ms                                                | 4.94 ms: 1.15x slower                                                 |
| docutils       | 1.43 sec                                               | 1.66 sec: 1.16x slower                                                |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 259 ms: 1.36x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 206 ms: 1.34x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 564 ms: 1.28x faster                                                  |
| async_tree_none            | 282 ms                                                 | 221 ms: 1.28x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 272 ms: 1.24x faster                                                  |
| async_tree_io              | 697 ms                                                 | 573 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 458 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 480 ms: 1.08x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                  |
| float          | 50.8 ms                                                | 60.5 ms: 1.19x slower                                                 |
| nbody          | 61.7 ms                                                | 77.3 ms: 1.25x slower                                                 |
| Geometric mean | (ref)                                                  | 1.15x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| regex_effbot   | 2.43 ms                                                | 2.59 ms: 1.07x slower                                                 |
| regex_v8       | 15.1 ms                                                | 17.6 ms: 1.16x slower                                                 |
| regex_compile  | 72.8 ms                                                | 95.7 ms: 1.31x slower                                                 |
| Geometric mean | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.53 ms: 1.15x faster                                                 |
| xml_etree_parse      | 100 ms                                                 | 106 ms: 1.06x slower                                                  |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.06x slower                                                 |
| pickle               | 6.98 us                                                | 7.47 us: 1.07x slower                                                 |
| unpickle_list        | 2.69 us                                                | 2.88 us: 1.07x slower                                                 |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                                 |
| pickle_list          | 2.70 us                                                | 2.97 us: 1.10x slower                                                 |
| xml_etree_iterparse  | 68.3 ms                                                | 76.5 ms: 1.12x slower                                                 |
| unpickle             | 8.29 us                                                | 9.39 us: 1.13x slower                                                 |
| unpickle_pure_python | 149 us                                                 | 176 us: 1.18x slower                                                  |
| pickle_pure_python   | 191 us                                                 | 228 us: 1.19x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 41.1 ms: 1.23x slower                                                 |
| xml_etree_generate   | 45.8 ms                                                | 58.7 ms: 1.28x slower                                                 |
| tomli_loads          | 1.27 sec                                               | 1.64 sec: 1.29x slower                                                |
| Geometric mean       | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 14.2 ms: 1.32x slower                                                 |
| python_startup_no_site | 8.57 ms                                                | 11.7 ms: 1.37x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 9.09 ms: 1.15x slower                                                 |
| django_template | 20.1 ms                                                | 23.8 ms: 1.18x slower                                                 |
| genshi_text     | 14.4 ms                                                | 17.3 ms: 1.20x slower                                                 |
| genshi_xml      | 28.5 ms                                                | 36.0 ms: 1.26x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.20x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 108 us: 2.80x faster                                                  |
| asyncio_tcp                | 643 ms                                                 | 418 ms: 1.54x faster                                                  |
| async_tree_memoization_tg  | 352 ms                                                 | 259 ms: 1.36x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 206 ms: 1.34x faster                                                  |
| pylint                     | 253 ms                                                 | 195 ms: 1.30x faster                                                  |
| generators                 | 30.3 ms                                                | 23.6 ms: 1.29x faster                                                 |
| async_tree_io_tg           | 724 ms                                                 | 564 ms: 1.28x faster                                                  |
| async_tree_none            | 282 ms                                                 | 221 ms: 1.28x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 272 ms: 1.24x faster                                                  |
| async_tree_io              | 697 ms                                                 | 573 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 458 ms: 1.20x faster                                                  |
| raytrace                   | 206 ms                                                 | 175 ms: 1.17x faster                                                  |
| json_dumps                 | 7.53 ms                                                | 6.53 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 480 ms: 1.08x faster                                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.30 sec: 1.08x faster                                                |
| logging_simple             | 3.41 us                                                | 3.18 us: 1.07x faster                                                 |
| coroutines                 | 17.2 ms                                                | 16.1 ms: 1.07x faster                                                 |
| logging_format             | 3.67 us                                                | 3.45 us: 1.07x faster                                                 |
| pathlib                    | 23.2 ms                                                | 22.5 ms: 1.03x faster                                                 |
| chaos                      | 47.4 ms                                                | 47.0 ms: 1.01x faster                                                 |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                                 |
| dask                       | 219 ms                                                 | 227 ms: 1.04x slower                                                  |
| coverage                   | 43.9 ms                                                | 45.7 ms: 1.04x slower                                                 |
| xml_etree_parse            | 100 ms                                                 | 106 ms: 1.06x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.06x slower                                                 |
| regex_effbot               | 2.43 ms                                                | 2.59 ms: 1.07x slower                                                 |
| deltablue                  | 2.75 ms                                                | 2.94 ms: 1.07x slower                                                 |
| thrift                     | 410 us                                                 | 439 us: 1.07x slower                                                  |
| pickle                     | 6.98 us                                                | 7.47 us: 1.07x slower                                                 |
| sympy_sum                  | 80.2 ms                                                | 85.9 ms: 1.07x slower                                                 |
| unpickle_list              | 2.69 us                                                | 2.88 us: 1.07x slower                                                 |
| sqlglot_parse              | 890 us                                                 | 957 us: 1.08x slower                                                  |
| json                       | 2.75 ms                                                | 3.00 ms: 1.09x slower                                                 |
| pycparser                  | 659 ms                                                 | 723 ms: 1.10x slower                                                  |
| sqlglot_transpile          | 1.05 ms                                                | 1.15 ms: 1.10x slower                                                 |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                                 |
| pickle_list                | 2.70 us                                                | 2.97 us: 1.10x slower                                                 |
| richards_super             | 37.3 ms                                                | 41.2 ms: 1.11x slower                                                 |
| mdp                        | 1.48 sec                                               | 1.64 sec: 1.11x slower                                                |
| go                         | 105 ms                                                 | 117 ms: 1.11x slower                                                  |
| sympy_integrate            | 11.3 ms                                                | 12.6 ms: 1.12x slower                                                 |
| xml_etree_iterparse        | 68.3 ms                                                | 76.5 ms: 1.12x slower                                                 |
| meteor_contest             | 71.1 ms                                                | 80.1 ms: 1.13x slower                                                 |
| bench_thread_pool          | 465 us                                                 | 525 us: 1.13x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.39 us: 1.13x slower                                                 |
| sympy_str                  | 144 ms                                                 | 164 ms: 1.14x slower                                                  |
| mako                       | 7.93 ms                                                | 9.09 ms: 1.15x slower                                                 |
| chameleon                  | 4.30 ms                                                | 4.94 ms: 1.15x slower                                                 |
| bench_mp_pool              | 41.0 ms                                                | 47.1 ms: 1.15x slower                                                 |
| deepcopy                   | 215 us                                                 | 248 us: 1.15x slower                                                  |
| sympy_expand               | 229 ms                                                 | 266 ms: 1.16x slower                                                  |
| regex_v8                   | 15.1 ms                                                | 17.6 ms: 1.16x slower                                                 |
| docutils                   | 1.43 sec                                               | 1.66 sec: 1.16x slower                                                |
| deepcopy_reduce            | 1.79 us                                                | 2.11 us: 1.18x slower                                                 |
| 2to3                       | 154 ms                                                 | 182 ms: 1.18x slower                                                  |
| unpickle_pure_python       | 149 us                                                 | 176 us: 1.18x slower                                                  |
| django_template            | 20.1 ms                                                | 23.8 ms: 1.18x slower                                                 |
| pickle_pure_python         | 191 us                                                 | 228 us: 1.19x slower                                                  |
| float                      | 50.8 ms                                                | 60.5 ms: 1.19x slower                                                 |
| comprehensions             | 14.4 us                                                | 17.3 us: 1.20x slower                                                 |
| genshi_text                | 14.4 ms                                                | 17.3 ms: 1.20x slower                                                 |
| pprint_pformat             | 979 ms                                                 | 1.18 sec: 1.20x slower                                                |
| pprint_safe_repr           | 478 ms                                                 | 578 ms: 1.21x slower                                                  |
| richards                   | 31.1 ms                                                | 37.6 ms: 1.21x slower                                                 |
| xml_etree_process          | 33.6 ms                                                | 41.1 ms: 1.23x slower                                                 |
| nqueens                    | 55.9 ms                                                | 69.1 ms: 1.24x slower                                                 |
| nbody                      | 61.7 ms                                                | 77.3 ms: 1.25x slower                                                 |
| sqlglot_optimize           | 29.6 ms                                                | 37.2 ms: 1.25x slower                                                 |
| deepcopy_memo              | 25.7 us                                                | 32.4 us: 1.26x slower                                                 |
| genshi_xml                 | 28.5 ms                                                | 36.0 ms: 1.26x slower                                                 |
| xml_etree_generate         | 45.8 ms                                                | 58.7 ms: 1.28x slower                                                 |
| sqlite_synth               | 1.26 us                                                | 1.61 us: 1.28x slower                                                 |
| tomli_loads                | 1.27 sec                                               | 1.64 sec: 1.29x slower                                                |
| create_gc_cycles           | 711 us                                                 | 914 us: 1.29x slower                                                  |
| crypto_pyaes               | 47.5 ms                                                | 61.2 ms: 1.29x slower                                                 |
| hexiom                     | 4.58 ms                                                | 6.00 ms: 1.31x slower                                                 |
| regex_compile              | 72.8 ms                                                | 95.7 ms: 1.31x slower                                                 |
| python_startup             | 10.8 ms                                                | 14.2 ms: 1.32x slower                                                 |
| fannkuch                   | 240 ms                                                 | 318 ms: 1.33x slower                                                  |
| scimark_fft                | 173 ms                                                 | 232 ms: 1.34x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 108 ms: 1.36x slower                                                  |
| python_startup_no_site     | 8.57 ms                                                | 11.7 ms: 1.37x slower                                                 |
| scimark_monte_carlo        | 43.5 ms                                                | 61.1 ms: 1.40x slower                                                 |
| pyflate                    | 284 ms                                                 | 399 ms: 1.41x slower                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 4.01 ms: 1.42x slower                                                 |
| spectral_norm              | 65.7 ms                                                | 94.2 ms: 1.43x slower                                                 |
| logging_silent             | 66.5 ns                                                | 95.4 ns: 1.43x slower                                                 |
| scimark_lu                 | 67.7 ms                                                | 98.1 ms: 1.45x slower                                                 |
| flaskblogging              | 2.35 ms                                                | 3.57 ms: 1.52x slower                                                 |
| async_generators           | 192 ms                                                 | 296 ms: 1.54x slower                                                  |
| telco                      | 3.17 ms                                                | 5.12 ms: 1.62x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (3): html5lib, asyncio_websockets, tornado_http
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dulwich_log, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
Ignored benchmarks (8) of results/bm-20240518-3.14.0a0-caf6064-PYTHON_UOPS/bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 0.49x