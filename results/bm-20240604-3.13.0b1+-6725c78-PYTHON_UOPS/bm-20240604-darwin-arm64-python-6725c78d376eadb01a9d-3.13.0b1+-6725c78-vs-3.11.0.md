# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: darwin-arm64
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 0.68x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 181 ms: 1.18x slower                                                   |
| chameleon      | 4.30 ms                                                | 4.96 ms: 1.15x slower                                                  |
| docutils       | 1.43 sec                                               | 1.66 sec: 1.16x slower                                                 |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 257 ms: 1.37x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 203 ms: 1.36x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 549 ms: 1.32x faster                                                   |
| async_tree_none            | 282 ms                                                 | 219 ms: 1.29x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 268 ms: 1.25x faster                                                   |
| async_tree_io              | 697 ms                                                 | 566 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 455 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 477 ms: 1.09x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| float          | 50.8 ms                                                | 60.5 ms: 1.19x slower                                                  |
| nbody          | 61.7 ms                                                | 77.4 ms: 1.25x slower                                                  |
| Geometric mean | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.6 ms: 1.16x slower                                                  |
| regex_compile  | 72.8 ms                                                | 95.8 ms: 1.32x slower                                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.56 ms: 1.15x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 107 ms: 1.06x slower                                                   |
| pickle_dict          | 17.1 us                                                | 18.3 us: 1.07x slower                                                  |
| pickle               | 6.98 us                                                | 7.51 us: 1.08x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.93 us: 1.09x slower                                                  |
| pickle_list          | 2.70 us                                                | 2.97 us: 1.10x slower                                                  |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| unpickle             | 8.29 us                                                | 9.26 us: 1.12x slower                                                  |
| xml_etree_iterparse  | 68.3 ms                                                | 76.4 ms: 1.12x slower                                                  |
| pickle_pure_python   | 191 us                                                 | 225 us: 1.18x slower                                                   |
| unpickle_pure_python | 149 us                                                 | 175 us: 1.18x slower                                                   |
| xml_etree_process    | 33.6 ms                                                | 41.0 ms: 1.22x slower                                                  |
| tomli_loads          | 1.27 sec                                               | 1.62 sec: 1.27x slower                                                 |
| xml_etree_generate   | 45.8 ms                                                | 58.8 ms: 1.28x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 8.57 ms                                                | 11.5 ms: 1.34x slower                                                  |
| python_startup         | 10.8 ms                                                | 14.5 ms: 1.35x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 8.85 ms: 1.12x slower                                                  |
| django_template | 20.1 ms                                                | 23.7 ms: 1.18x slower                                                  |
| genshi_text     | 14.4 ms                                                | 17.3 ms: 1.20x slower                                                  |
| genshi_xml      | 28.5 ms                                                | 35.8 ms: 1.25x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.19x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 106 us: 2.84x faster                                                   |
| asyncio_tcp                | 643 ms                                                 | 438 ms: 1.47x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 257 ms: 1.37x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 203 ms: 1.36x faster                                                   |
| pylint                     | 253 ms                                                 | 191 ms: 1.32x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 549 ms: 1.32x faster                                                   |
| generators                 | 30.3 ms                                                | 23.5 ms: 1.29x faster                                                  |
| async_tree_none            | 282 ms                                                 | 219 ms: 1.29x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 268 ms: 1.25x faster                                                   |
| async_tree_io              | 697 ms                                                 | 566 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 455 ms: 1.21x faster                                                   |
| json_dumps                 | 7.53 ms                                                | 6.56 ms: 1.15x faster                                                  |
| raytrace                   | 206 ms                                                 | 180 ms: 1.14x faster                                                   |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.24 sec: 1.13x faster                                                 |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 477 ms: 1.09x faster                                                   |
| logging_simple             | 3.41 us                                                | 3.17 us: 1.08x faster                                                  |
| logging_format             | 3.67 us                                                | 3.45 us: 1.06x faster                                                  |
| coroutines                 | 17.2 ms                                                | 16.2 ms: 1.06x faster                                                  |
| chaos                      | 47.4 ms                                                | 46.3 ms: 1.02x faster                                                  |
| pathlib                    | 23.2 ms                                                | 22.8 ms: 1.02x faster                                                  |
| pidigits                   | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                   |
| gunicorn                   | 1.10 ms                                                | 1.12 ms: 1.02x slower                                                  |
| aiohttp                    | 1.02 ms                                                | 1.05 ms: 1.03x slower                                                  |
| dulwich_log                | 28.6 ms                                                | 29.5 ms: 1.03x slower                                                  |
| coverage                   | 43.9 ms                                                | 45.3 ms: 1.03x slower                                                  |
| dask                       | 219 ms                                                 | 227 ms: 1.03x slower                                                   |
| gc_traversal               | 2.38 ms                                                | 2.47 ms: 1.04x slower                                                  |
| mdp                        | 1.48 sec                                               | 1.55 sec: 1.05x slower                                                 |
| regex_effbot               | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                  |
| xml_etree_parse            | 100 ms                                                 | 107 ms: 1.06x slower                                                   |
| sqlglot_parse              | 890 us                                                 | 947 us: 1.06x slower                                                   |
| sympy_sum                  | 80.2 ms                                                | 85.9 ms: 1.07x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.3 us: 1.07x slower                                                  |
| deltablue                  | 2.75 ms                                                | 2.95 ms: 1.07x slower                                                  |
| thrift                     | 410 us                                                 | 442 us: 1.08x slower                                                   |
| pickle                     | 6.98 us                                                | 7.51 us: 1.08x slower                                                  |
| sqlglot_transpile          | 1.05 ms                                                | 1.14 ms: 1.09x slower                                                  |
| richards_super             | 37.3 ms                                                | 40.6 ms: 1.09x slower                                                  |
| unpickle_list              | 2.69 us                                                | 2.93 us: 1.09x slower                                                  |
| json                       | 2.75 ms                                                | 3.01 ms: 1.09x slower                                                  |
| pickle_list                | 2.70 us                                                | 2.97 us: 1.10x slower                                                  |
| pycparser                  | 659 ms                                                 | 727 ms: 1.10x slower                                                   |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| meteor_contest             | 71.1 ms                                                | 78.8 ms: 1.11x slower                                                  |
| go                         | 105 ms                                                 | 117 ms: 1.11x slower                                                   |
| sympy_integrate            | 11.3 ms                                                | 12.6 ms: 1.12x slower                                                  |
| mako                       | 7.93 ms                                                | 8.85 ms: 1.12x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.26 us: 1.12x slower                                                  |
| xml_etree_iterparse        | 68.3 ms                                                | 76.4 ms: 1.12x slower                                                  |
| bench_thread_pool          | 465 us                                                 | 521 us: 1.12x slower                                                   |
| sympy_str                  | 144 ms                                                 | 163 ms: 1.14x slower                                                   |
| mypy2                      | 372 ms                                                 | 429 ms: 1.15x slower                                                   |
| sympy_expand               | 229 ms                                                 | 264 ms: 1.15x slower                                                   |
| chameleon                  | 4.30 ms                                                | 4.96 ms: 1.15x slower                                                  |
| regex_v8                   | 15.1 ms                                                | 17.6 ms: 1.16x slower                                                  |
| docutils                   | 1.43 sec                                               | 1.66 sec: 1.16x slower                                                 |
| deepcopy                   | 215 us                                                 | 251 us: 1.16x slower                                                   |
| bench_mp_pool              | 41.0 ms                                                | 47.8 ms: 1.17x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 2.10 us: 1.17x slower                                                  |
| pickle_pure_python         | 191 us                                                 | 225 us: 1.18x slower                                                   |
| 2to3                       | 154 ms                                                 | 181 ms: 1.18x slower                                                   |
| django_template            | 20.1 ms                                                | 23.7 ms: 1.18x slower                                                  |
| unpickle_pure_python       | 149 us                                                 | 175 us: 1.18x slower                                                   |
| float                      | 50.8 ms                                                | 60.5 ms: 1.19x slower                                                  |
| pprint_pformat             | 979 ms                                                 | 1.17 sec: 1.19x slower                                                 |
| pprint_safe_repr           | 478 ms                                                 | 571 ms: 1.19x slower                                                   |
| richards                   | 31.1 ms                                                | 37.2 ms: 1.20x slower                                                  |
| comprehensions             | 14.4 us                                                | 17.3 us: 1.20x slower                                                  |
| genshi_text                | 14.4 ms                                                | 17.3 ms: 1.20x slower                                                  |
| nqueens                    | 55.9 ms                                                | 68.0 ms: 1.22x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 41.0 ms: 1.22x slower                                                  |
| sqlglot_optimize           | 29.6 ms                                                | 37.2 ms: 1.25x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 35.8 ms: 1.25x slower                                                  |
| nbody                      | 61.7 ms                                                | 77.4 ms: 1.25x slower                                                  |
| deepcopy_memo              | 25.7 us                                                | 32.6 us: 1.26x slower                                                  |
| tomli_loads                | 1.27 sec                                               | 1.62 sec: 1.27x slower                                                 |
| xml_etree_generate         | 45.8 ms                                                | 58.8 ms: 1.28x slower                                                  |
| crypto_pyaes               | 47.5 ms                                                | 61.0 ms: 1.28x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 913 us: 1.28x slower                                                   |
| sqlite_synth               | 1.26 us                                                | 1.62 us: 1.29x slower                                                  |
| scimark_fft                | 173 ms                                                 | 223 ms: 1.29x slower                                                   |
| hexiom                     | 4.58 ms                                                | 5.94 ms: 1.30x slower                                                  |
| fannkuch                   | 240 ms                                                 | 312 ms: 1.30x slower                                                   |
| regex_compile              | 72.8 ms                                                | 95.8 ms: 1.32x slower                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.77 ms: 1.34x slower                                                  |
| python_startup_no_site     | 8.57 ms                                                | 11.5 ms: 1.34x slower                                                  |
| python_startup             | 10.8 ms                                                | 14.5 ms: 1.35x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 107 ms: 1.36x slower                                                   |
| flaskblogging              | 2.35 ms                                                | 3.26 ms: 1.39x slower                                                  |
| scimark_monte_carlo        | 43.5 ms                                                | 60.5 ms: 1.39x slower                                                  |
| pyflate                    | 284 ms                                                 | 396 ms: 1.40x slower                                                   |
| spectral_norm              | 65.7 ms                                                | 93.4 ms: 1.42x slower                                                  |
| logging_silent             | 66.5 ns                                                | 95.1 ns: 1.43x slower                                                  |
| scimark_lu                 | 67.7 ms                                                | 97.0 ms: 1.43x slower                                                  |
| async_generators           | 192 ms                                                 | 297 ms: 1.55x slower                                                   |
| telco                      | 3.17 ms                                                | 4.95 ms: 1.56x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (3): asyncio_websockets, tornado_http, html5lib
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
Ignored benchmarks (8) of results/bm-20240604-3.13.0b1+-6725c78-PYTHON_UOPS/bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 0.68x