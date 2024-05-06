# Results vs. 3.11.0

- fork: savannahostrowski
- ref: llvm_18
- machine: darwin-arm64
- commit hash: b2bbeb0
- commit date: 2024-04-27
- overall geometric mean: 1.01x faster
- HPT reliability: 75.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 183 ms: 1.19x slower                                                 |
| chameleon      | 4.30 ms                                                | 4.45 ms: 1.04x slower                                                |
| docutils       | 1.43 sec                                               | 1.50 sec: 1.05x slower                                               |
| html5lib       | 33.0 ms                                                | 30.7 ms: 1.07x faster                                                |
| Geometric mean | (ref)                                                  | 1.04x slower                                                         |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 282 ms                                                 | 198 ms: 1.42x faster                                                 |
| async_tree_none_tg         | 276 ms                                                 | 195 ms: 1.41x faster                                                 |
| async_tree_memoization_tg  | 352 ms                                                 | 259 ms: 1.36x faster                                                 |
| async_tree_io_tg           | 724 ms                                                 | 558 ms: 1.30x faster                                                 |
| async_tree_memoization     | 336 ms                                                 | 268 ms: 1.25x faster                                                 |
| async_tree_io              | 697 ms                                                 | 558 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 463 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 457 ms: 1.14x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.29x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                 |
| nbody          | 61.7 ms                                                | 67.9 ms: 1.10x slower                                                |
| Geometric mean | (ref)                                                  | 1.03x slower                                                         |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 72.1 ms: 1.01x faster                                                |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                 |
| regex_effbot   | 2.43 ms                                                | 2.58 ms: 1.06x slower                                                |
| regex_v8       | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                |
| Geometric mean | (ref)                                                  | 1.05x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.31 ms: 1.19x faster                                                |
| unpickle_pure_python | 149 us                                                 | 132 us: 1.13x faster                                                 |
| pickle_pure_python   | 191 us                                                 | 182 us: 1.05x faster                                                 |
| tomli_loads          | 1.27 sec                                               | 1.23 sec: 1.03x faster                                               |
| xml_etree_parse      | 100 ms                                                 | 104 ms: 1.04x slower                                                 |
| xml_etree_iterparse  | 68.3 ms                                                | 70.7 ms: 1.04x slower                                                |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.06x slower                                                |
| pickle               | 6.98 us                                                | 7.48 us: 1.07x slower                                                |
| unpickle_list        | 2.69 us                                                | 2.91 us: 1.08x slower                                                |
| xml_etree_process    | 33.6 ms                                                | 36.5 ms: 1.09x slower                                                |
| pickle_list          | 2.70 us                                                | 2.98 us: 1.10x slower                                                |
| json_loads           | 15.3 us                                                | 17.0 us: 1.11x slower                                                |
| unpickle             | 8.29 us                                                | 9.29 us: 1.12x slower                                                |
| xml_etree_generate   | 45.8 ms                                                | 53.6 ms: 1.17x slower                                                |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 8.57 ms                                                | 11.1 ms: 1.30x slower                                                |
| python_startup         | 10.8 ms                                                | 14.1 ms: 1.31x slower                                                |
| Geometric mean         | (ref)                                                  | 1.31x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.40 ms: 1.24x faster                                                |
| django_template | 20.1 ms                                                | 20.8 ms: 1.03x slower                                                |
| genshi_text     | 14.4 ms                                                | 15.6 ms: 1.08x slower                                                |
| genshi_xml      | 28.5 ms                                                | 35.9 ms: 1.26x slower                                                |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 103 us: 2.91x faster                                                 |
| asyncio_tcp                | 643 ms                                                 | 431 ms: 1.49x faster                                                 |
| pylint                     | 253 ms                                                 | 177 ms: 1.42x faster                                                 |
| async_tree_none            | 282 ms                                                 | 198 ms: 1.42x faster                                                 |
| async_tree_none_tg         | 276 ms                                                 | 195 ms: 1.41x faster                                                 |
| async_tree_memoization_tg  | 352 ms                                                 | 259 ms: 1.36x faster                                                 |
| async_tree_io_tg           | 724 ms                                                 | 558 ms: 1.30x faster                                                 |
| async_tree_memoization     | 336 ms                                                 | 268 ms: 1.25x faster                                                 |
| async_tree_io              | 697 ms                                                 | 558 ms: 1.25x faster                                                 |
| mako                       | 7.93 ms                                                | 6.40 ms: 1.24x faster                                                |
| raytrace                   | 206 ms                                                 | 169 ms: 1.22x faster                                                 |
| json_dumps                 | 7.53 ms                                                | 6.31 ms: 1.19x faster                                                |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 463 ms: 1.19x faster                                                 |
| chaos                      | 47.4 ms                                                | 40.4 ms: 1.17x faster                                                |
| sqlglot_parse              | 890 us                                                 | 772 us: 1.15x faster                                                 |
| comprehensions             | 14.4 us                                                | 12.6 us: 1.15x faster                                                |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 457 ms: 1.14x faster                                                 |
| deltablue                  | 2.75 ms                                                | 2.43 ms: 1.13x faster                                                |
| unpickle_pure_python       | 149 us                                                 | 132 us: 1.13x faster                                                 |
| generators                 | 30.3 ms                                                | 26.9 ms: 1.12x faster                                                |
| sqlglot_transpile          | 1.05 ms                                                | 942 us: 1.12x faster                                                 |
| richards_super             | 37.3 ms                                                | 33.8 ms: 1.10x faster                                                |
| sympy_sum                  | 80.2 ms                                                | 72.8 ms: 1.10x faster                                                |
| logging_simple             | 3.41 us                                                | 3.12 us: 1.09x faster                                                |
| logging_format             | 3.67 us                                                | 3.38 us: 1.09x faster                                                |
| html5lib                   | 33.0 ms                                                | 30.7 ms: 1.07x faster                                                |
| deepcopy_memo              | 25.7 us                                                | 24.1 us: 1.07x faster                                                |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.32 sec: 1.06x faster                                               |
| sympy_str                  | 144 ms                                                 | 136 ms: 1.05x faster                                                 |
| coroutines                 | 17.2 ms                                                | 16.3 ms: 1.05x faster                                                |
| pickle_pure_python         | 191 us                                                 | 182 us: 1.05x faster                                                 |
| richards                   | 31.1 ms                                                | 29.8 ms: 1.04x faster                                                |
| logging_silent             | 66.5 ns                                                | 64.2 ns: 1.04x faster                                                |
| sympy_integrate            | 11.3 ms                                                | 10.9 ms: 1.04x faster                                                |
| tomli_loads                | 1.27 sec                                               | 1.23 sec: 1.03x faster                                               |
| pycparser                  | 659 ms                                                 | 642 ms: 1.03x faster                                                 |
| hexiom                     | 4.58 ms                                                | 4.48 ms: 1.02x faster                                                |
| fannkuch                   | 240 ms                                                 | 236 ms: 1.01x faster                                                 |
| go                         | 105 ms                                                 | 104 ms: 1.01x faster                                                 |
| regex_compile              | 72.8 ms                                                | 72.1 ms: 1.01x faster                                                |
| deepcopy                   | 215 us                                                 | 213 us: 1.01x faster                                                 |
| pprint_safe_repr           | 478 ms                                                 | 475 ms: 1.01x faster                                                 |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                 |
| dulwich_log                | 28.6 ms                                                | 28.8 ms: 1.01x slower                                                |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                 |
| sympy_expand               | 229 ms                                                 | 233 ms: 1.02x slower                                                 |
| meteor_contest             | 71.1 ms                                                | 72.8 ms: 1.02x slower                                                |
| mdp                        | 1.48 sec                                               | 1.52 sec: 1.03x slower                                               |
| scimark_monte_carlo        | 43.5 ms                                                | 44.7 ms: 1.03x slower                                                |
| crypto_pyaes               | 47.5 ms                                                | 48.9 ms: 1.03x slower                                                |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                                |
| django_template            | 20.1 ms                                                | 20.8 ms: 1.03x slower                                                |
| coverage                   | 43.9 ms                                                | 45.3 ms: 1.03x slower                                                |
| xml_etree_parse            | 100 ms                                                 | 104 ms: 1.04x slower                                                 |
| xml_etree_iterparse        | 68.3 ms                                                | 70.7 ms: 1.04x slower                                                |
| chameleon                  | 4.30 ms                                                | 4.45 ms: 1.04x slower                                                |
| deepcopy_reduce            | 1.79 us                                                | 1.86 us: 1.04x slower                                                |
| nqueens                    | 55.9 ms                                                | 58.3 ms: 1.04x slower                                                |
| bench_thread_pool          | 465 us                                                 | 487 us: 1.05x slower                                                 |
| docutils                   | 1.43 sec                                               | 1.50 sec: 1.05x slower                                               |
| gunicorn                   | 1.10 ms                                                | 1.16 ms: 1.06x slower                                                |
| json                       | 2.75 ms                                                | 2.91 ms: 1.06x slower                                                |
| aiohttp                    | 1.02 ms                                                | 1.09 ms: 1.06x slower                                                |
| regex_effbot               | 2.43 ms                                                | 2.58 ms: 1.06x slower                                                |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.06x slower                                                |
| spectral_norm              | 65.7 ms                                                | 70.3 ms: 1.07x slower                                                |
| thrift                     | 410 us                                                 | 439 us: 1.07x slower                                                 |
| pickle                     | 6.98 us                                                | 7.48 us: 1.07x slower                                                |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.03 ms: 1.08x slower                                                |
| genshi_text                | 14.4 ms                                                | 15.6 ms: 1.08x slower                                                |
| unpickle_list              | 2.69 us                                                | 2.91 us: 1.08x slower                                                |
| xml_etree_process          | 33.6 ms                                                | 36.5 ms: 1.09x slower                                                |
| sqlglot_normalize          | 162 ms                                                 | 176 ms: 1.09x slower                                                 |
| nbody                      | 61.7 ms                                                | 67.9 ms: 1.10x slower                                                |
| pickle_list                | 2.70 us                                                | 2.98 us: 1.10x slower                                                |
| json_loads                 | 15.3 us                                                | 17.0 us: 1.11x slower                                                |
| scimark_fft                | 173 ms                                                 | 192 ms: 1.11x slower                                                 |
| pyflate                    | 284 ms                                                 | 317 ms: 1.12x slower                                                 |
| unpickle                   | 8.29 us                                                | 9.29 us: 1.12x slower                                                |
| sqlglot_optimize           | 29.6 ms                                                | 33.3 ms: 1.12x slower                                                |
| bench_mp_pool              | 41.0 ms                                                | 46.2 ms: 1.13x slower                                                |
| regex_v8                   | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                |
| xml_etree_generate         | 45.8 ms                                                | 53.6 ms: 1.17x slower                                                |
| scimark_lu                 | 67.7 ms                                                | 80.0 ms: 1.18x slower                                                |
| 2to3                       | 154 ms                                                 | 183 ms: 1.19x slower                                                 |
| sqlite_synth               | 1.26 us                                                | 1.57 us: 1.25x slower                                                |
| genshi_xml                 | 28.5 ms                                                | 35.9 ms: 1.26x slower                                                |
| create_gc_cycles           | 711 us                                                 | 908 us: 1.28x slower                                                 |
| python_startup_no_site     | 8.57 ms                                                | 11.1 ms: 1.30x slower                                                |
| mypy2                      | 372 ms                                                 | 487 ms: 1.31x slower                                                 |
| python_startup             | 10.8 ms                                                | 14.1 ms: 1.31x slower                                                |
| scimark_sor                | 79.2 ms                                                | 104 ms: 1.31x slower                                                 |
| telco                      | 3.17 ms                                                | 4.46 ms: 1.41x slower                                                |
| async_generators           | 192 ms                                                 | 294 ms: 1.53x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (6): float, asyncio_websockets, pprint_pformat, pathlib, dask, tornado_http
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240427-3.13.0a6+-b2bbeb0-JIT/bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 75.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x