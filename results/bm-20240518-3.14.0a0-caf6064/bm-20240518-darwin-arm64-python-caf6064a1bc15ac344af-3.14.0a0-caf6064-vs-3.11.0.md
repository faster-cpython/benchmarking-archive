# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: darwin-arm64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.04x faster
- HPT reliability: 93.62%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.52x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 182 ms: 1.18x slower                                                  |
| chameleon      | 4.30 ms                                                | 4.29 ms: 1.00x faster                                                 |
| docutils       | 1.43 sec                                               | 1.44 sec: 1.00x slower                                                |
| html5lib       | 33.0 ms                                                | 31.0 ms: 1.07x faster                                                 |
| tornado_http   | 69.1 ms                                                | 66.2 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 239 ms: 1.48x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 197 ms: 1.40x faster                                                  |
| async_tree_none            | 282 ms                                                 | 209 ms: 1.35x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 258 ms: 1.30x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 565 ms: 1.28x faster                                                  |
| async_tree_io              | 697 ms                                                 | 566 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 451 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 468 ms: 1.11x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.29x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 48.2 ms: 1.05x faster                                                 |
| nbody          | 61.7 ms                                                | 60.3 ms: 1.02x faster                                                 |
| pidigits       | 280 ms                                                 | 281 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 68.2 ms: 1.07x faster                                                 |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| regex_effbot   | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                 |
| regex_v8       | 15.1 ms                                                | 17.3 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.29 ms: 1.20x faster                                                 |
| pickle_pure_python   | 191 us                                                 | 178 us: 1.07x faster                                                  |
| unpickle_pure_python | 149 us                                                 | 140 us: 1.06x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 104 ms: 1.04x slower                                                  |
| xml_etree_iterparse  | 68.3 ms                                                | 71.6 ms: 1.05x slower                                                 |
| pickle               | 6.98 us                                                | 7.45 us: 1.07x slower                                                 |
| pickle_dict          | 17.1 us                                                | 18.3 us: 1.07x slower                                                 |
| unpickle_list        | 2.69 us                                                | 2.90 us: 1.08x slower                                                 |
| xml_etree_process    | 33.6 ms                                                | 36.9 ms: 1.10x slower                                                 |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                                 |
| pickle_list          | 2.70 us                                                | 3.00 us: 1.11x slower                                                 |
| unpickle             | 8.29 us                                                | 9.33 us: 1.12x slower                                                 |
| xml_etree_generate   | 45.8 ms                                                | 52.2 ms: 1.14x slower                                                 |
| tomli_loads          | 1.27 sec                                               | 1.46 sec: 1.14x slower                                                |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 14.0 ms: 1.31x slower                                                 |
| python_startup_no_site | 8.57 ms                                                | 11.5 ms: 1.34x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.32x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.91 ms: 1.15x faster                                                 |
| genshi_text     | 14.4 ms                                                | 13.7 ms: 1.05x faster                                                 |
| django_template | 20.1 ms                                                | 19.4 ms: 1.04x faster                                                 |
| genshi_xml      | 28.5 ms                                                | 29.7 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 91.7 us: 3.28x faster                                                 |
| asyncio_tcp                | 643 ms                                                 | 425 ms: 1.51x faster                                                  |
| async_tree_memoization_tg  | 352 ms                                                 | 239 ms: 1.48x faster                                                  |
| pylint                     | 253 ms                                                 | 172 ms: 1.47x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 197 ms: 1.40x faster                                                  |
| raytrace                   | 206 ms                                                 | 147 ms: 1.40x faster                                                  |
| chaos                      | 47.4 ms                                                | 34.3 ms: 1.38x faster                                                 |
| comprehensions             | 14.4 us                                                | 10.7 us: 1.36x faster                                                 |
| async_tree_none            | 282 ms                                                 | 209 ms: 1.35x faster                                                  |
| generators                 | 30.3 ms                                                | 22.9 ms: 1.33x faster                                                 |
| async_tree_memoization     | 336 ms                                                 | 258 ms: 1.30x faster                                                  |
| deltablue                  | 2.75 ms                                                | 2.14 ms: 1.29x faster                                                 |
| async_tree_io_tg           | 724 ms                                                 | 565 ms: 1.28x faster                                                  |
| async_tree_io              | 697 ms                                                 | 566 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 451 ms: 1.22x faster                                                  |
| sqlglot_parse              | 890 us                                                 | 733 us: 1.21x faster                                                  |
| json_dumps                 | 7.53 ms                                                | 6.29 ms: 1.20x faster                                                 |
| sqlglot_transpile          | 1.05 ms                                                | 892 us: 1.18x faster                                                  |
| mako                       | 7.93 ms                                                | 6.91 ms: 1.15x faster                                                 |
| sympy_sum                  | 80.2 ms                                                | 69.9 ms: 1.15x faster                                                 |
| deepcopy_memo              | 25.7 us                                                | 22.6 us: 1.14x faster                                                 |
| hexiom                     | 4.58 ms                                                | 4.08 ms: 1.12x faster                                                 |
| logging_simple             | 3.41 us                                                | 3.07 us: 1.11x faster                                                 |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 468 ms: 1.11x faster                                                  |
| logging_silent             | 66.5 ns                                                | 60.0 ns: 1.11x faster                                                 |
| logging_format             | 3.67 us                                                | 3.35 us: 1.10x faster                                                 |
| sympy_str                  | 144 ms                                                 | 132 ms: 1.09x faster                                                  |
| sympy_integrate            | 11.3 ms                                                | 10.3 ms: 1.09x faster                                                 |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.28 sec: 1.09x faster                                                |
| richards_super             | 37.3 ms                                                | 34.3 ms: 1.09x faster                                                 |
| coroutines                 | 17.2 ms                                                | 15.9 ms: 1.08x faster                                                 |
| deepcopy                   | 215 us                                                 | 200 us: 1.08x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 178 us: 1.07x faster                                                  |
| regex_compile              | 72.8 ms                                                | 68.2 ms: 1.07x faster                                                 |
| html5lib                   | 33.0 ms                                                | 31.0 ms: 1.07x faster                                                 |
| nqueens                    | 55.9 ms                                                | 52.6 ms: 1.06x faster                                                 |
| unpickle_pure_python       | 149 us                                                 | 140 us: 1.06x faster                                                  |
| float                      | 50.8 ms                                                | 48.2 ms: 1.05x faster                                                 |
| go                         | 105 ms                                                 | 100 ms: 1.05x faster                                                  |
| genshi_text                | 14.4 ms                                                | 13.7 ms: 1.05x faster                                                 |
| pycparser                  | 659 ms                                                 | 632 ms: 1.04x faster                                                  |
| tornado_http               | 69.1 ms                                                | 66.2 ms: 1.04x faster                                                 |
| pprint_pformat             | 979 ms                                                 | 943 ms: 1.04x faster                                                  |
| django_template            | 20.1 ms                                                | 19.4 ms: 1.04x faster                                                 |
| pprint_safe_repr           | 478 ms                                                 | 462 ms: 1.03x faster                                                  |
| pathlib                    | 23.2 ms                                                | 22.5 ms: 1.03x faster                                                 |
| scimark_monte_carlo        | 43.5 ms                                                | 42.2 ms: 1.03x faster                                                 |
| nbody                      | 61.7 ms                                                | 60.3 ms: 1.02x faster                                                 |
| meteor_contest             | 71.1 ms                                                | 69.8 ms: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.77 ms: 1.02x faster                                                 |
| scimark_lu                 | 67.7 ms                                                | 66.8 ms: 1.01x faster                                                 |
| sympy_expand               | 229 ms                                                 | 227 ms: 1.01x faster                                                  |
| bench_thread_pool          | 465 us                                                 | 463 us: 1.00x faster                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.79 us: 1.00x faster                                                 |
| chameleon                  | 4.30 ms                                                | 4.29 ms: 1.00x faster                                                 |
| pidigits                   | 280 ms                                                 | 281 ms: 1.00x slower                                                  |
| docutils                   | 1.43 sec                                               | 1.44 sec: 1.00x slower                                                |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| mdp                        | 1.48 sec                                               | 1.49 sec: 1.01x slower                                                |
| spectral_norm              | 65.7 ms                                                | 67.2 ms: 1.02x slower                                                 |
| sqlglot_normalize          | 162 ms                                                 | 167 ms: 1.03x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                                 |
| xml_etree_parse            | 100 ms                                                 | 104 ms: 1.04x slower                                                  |
| fannkuch                   | 240 ms                                                 | 249 ms: 1.04x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 29.7 ms: 1.04x slower                                                 |
| thrift                     | 410 us                                                 | 428 us: 1.04x slower                                                  |
| crypto_pyaes               | 47.5 ms                                                | 49.6 ms: 1.05x slower                                                 |
| scimark_fft                | 173 ms                                                 | 180 ms: 1.05x slower                                                  |
| coverage                   | 43.9 ms                                                | 45.9 ms: 1.05x slower                                                 |
| sqlglot_optimize           | 29.6 ms                                                | 31.0 ms: 1.05x slower                                                 |
| xml_etree_iterparse        | 68.3 ms                                                | 71.6 ms: 1.05x slower                                                 |
| regex_effbot               | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                 |
| pickle                     | 6.98 us                                                | 7.45 us: 1.07x slower                                                 |
| pickle_dict                | 17.1 us                                                | 18.3 us: 1.07x slower                                                 |
| json                       | 2.75 ms                                                | 2.95 ms: 1.07x slower                                                 |
| unpickle_list              | 2.69 us                                                | 2.90 us: 1.08x slower                                                 |
| xml_etree_process          | 33.6 ms                                                | 36.9 ms: 1.10x slower                                                 |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                                 |
| pickle_list                | 2.70 us                                                | 3.00 us: 1.11x slower                                                 |
| bench_mp_pool              | 41.0 ms                                                | 45.7 ms: 1.12x slower                                                 |
| unpickle                   | 8.29 us                                                | 9.33 us: 1.12x slower                                                 |
| pyflate                    | 284 ms                                                 | 320 ms: 1.13x slower                                                  |
| xml_etree_generate         | 45.8 ms                                                | 52.2 ms: 1.14x slower                                                 |
| regex_v8                   | 15.1 ms                                                | 17.3 ms: 1.14x slower                                                 |
| tomli_loads                | 1.27 sec                                               | 1.46 sec: 1.14x slower                                                |
| 2to3                       | 154 ms                                                 | 182 ms: 1.18x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 94.0 ms: 1.19x slower                                                 |
| sqlite_synth               | 1.26 us                                                | 1.54 us: 1.23x slower                                                 |
| create_gc_cycles           | 711 us                                                 | 910 us: 1.28x slower                                                  |
| python_startup             | 10.8 ms                                                | 14.0 ms: 1.31x slower                                                 |
| python_startup_no_site     | 8.57 ms                                                | 11.5 ms: 1.34x slower                                                 |
| flaskblogging              | 2.35 ms                                                | 3.40 ms: 1.45x slower                                                 |
| async_generators           | 192 ms                                                 | 279 ms: 1.45x slower                                                  |
| telco                      | 3.17 ms                                                | 4.61 ms: 1.46x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (3): asyncio_websockets, richards, dask
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dulwich_log, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240518-3.14.0a0-caf6064/bm-20240518-darwin-arm64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 93.62% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.52x