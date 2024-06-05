# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: darwin-arm64
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.02x faster
- HPT reliability: 58.04%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.68x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 172 ms: 1.11x slower                                                   |
| chameleon      | 4.30 ms                                                | 4.41 ms: 1.03x slower                                                  |
| docutils       | 1.43 sec                                               | 1.50 sec: 1.05x slower                                                 |
| html5lib       | 33.0 ms                                                | 31.9 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 238 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 196 ms: 1.41x faster                                                   |
| async_tree_none            | 282 ms                                                 | 209 ms: 1.35x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 550 ms: 1.32x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 259 ms: 1.30x faster                                                   |
| async_tree_io              | 697 ms                                                 | 550 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 451 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 466 ms: 1.11x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.30x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 47.4 ms: 1.07x faster                                                  |
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| nbody          | 61.7 ms                                                | 63.6 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 72.7 ms: 1.00x faster                                                  |
| regex_dna      | 148 ms                                                 | 149 ms: 1.00x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.3 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.11 ms: 1.23x faster                                                  |
| unpickle_pure_python | 149 us                                                 | 131 us: 1.14x faster                                                   |
| pickle_pure_python   | 191 us                                                 | 173 us: 1.10x faster                                                   |
| tomli_loads          | 1.27 sec                                               | 1.25 sec: 1.02x faster                                                 |
| xml_etree_parse      | 100 ms                                                 | 102 ms: 1.01x slower                                                   |
| xml_etree_iterparse  | 68.3 ms                                                | 70.3 ms: 1.03x slower                                                  |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.07x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 35.9 ms: 1.07x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.88 us: 1.07x slower                                                  |
| pickle               | 6.98 us                                                | 7.49 us: 1.07x slower                                                  |
| unpickle             | 8.29 us                                                | 9.13 us: 1.10x slower                                                  |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| pickle_list          | 2.70 us                                                | 2.99 us: 1.11x slower                                                  |
| xml_etree_generate   | 45.8 ms                                                | 51.4 ms: 1.12x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 15.6 ms: 1.45x slower                                                  |
| python_startup_no_site | 8.57 ms                                                | 12.7 ms: 1.48x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.37 ms: 1.25x faster                                                  |
| django_template | 20.1 ms                                                | 21.3 ms: 1.06x slower                                                  |
| genshi_text     | 14.4 ms                                                | 16.0 ms: 1.11x slower                                                  |
| genshi_xml      | 28.5 ms                                                | 39.5 ms: 1.39x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 93.1 us: 3.23x faster                                                  |
| asyncio_tcp                | 643 ms                                                 | 419 ms: 1.54x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 238 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 196 ms: 1.41x faster                                                   |
| pylint                     | 253 ms                                                 | 180 ms: 1.40x faster                                                   |
| async_tree_none            | 282 ms                                                 | 209 ms: 1.35x faster                                                   |
| generators                 | 30.3 ms                                                | 23.0 ms: 1.32x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 550 ms: 1.32x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 259 ms: 1.30x faster                                                   |
| async_tree_io              | 697 ms                                                 | 550 ms: 1.27x faster                                                   |
| raytrace                   | 206 ms                                                 | 164 ms: 1.25x faster                                                   |
| mako                       | 7.93 ms                                                | 6.37 ms: 1.25x faster                                                  |
| json_dumps                 | 7.53 ms                                                | 6.11 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 451 ms: 1.22x faster                                                   |
| chaos                      | 47.4 ms                                                | 39.1 ms: 1.21x faster                                                  |
| deepcopy_memo              | 25.7 us                                                | 21.7 us: 1.19x faster                                                  |
| comprehensions             | 14.4 us                                                | 12.2 us: 1.19x faster                                                  |
| unpickle_pure_python       | 149 us                                                 | 131 us: 1.14x faster                                                   |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.24 sec: 1.13x faster                                                 |
| sympy_sum                  | 80.2 ms                                                | 71.9 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 466 ms: 1.11x faster                                                   |
| logging_simple             | 3.41 us                                                | 3.07 us: 1.11x faster                                                  |
| deltablue                  | 2.75 ms                                                | 2.48 ms: 1.11x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 173 us: 1.10x faster                                                   |
| logging_format             | 3.67 us                                                | 3.35 us: 1.10x faster                                                  |
| coroutines                 | 17.2 ms                                                | 15.9 ms: 1.08x faster                                                  |
| float                      | 50.8 ms                                                | 47.4 ms: 1.07x faster                                                  |
| sqlglot_parse              | 890 us                                                 | 831 us: 1.07x faster                                                   |
| logging_silent             | 66.5 ns                                                | 62.2 ns: 1.07x faster                                                  |
| richards_super             | 37.3 ms                                                | 35.2 ms: 1.06x faster                                                  |
| sympy_str                  | 144 ms                                                 | 137 ms: 1.05x faster                                                   |
| hexiom                     | 4.58 ms                                                | 4.37 ms: 1.05x faster                                                  |
| sqlglot_transpile          | 1.05 ms                                                | 1.01 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 478 ms                                                 | 459 ms: 1.04x faster                                                   |
| deepcopy                   | 215 us                                                 | 207 us: 1.04x faster                                                   |
| sympy_integrate            | 11.3 ms                                                | 10.9 ms: 1.04x faster                                                  |
| mdp                        | 1.48 sec                                               | 1.44 sec: 1.03x faster                                                 |
| pprint_pformat             | 979 ms                                                 | 947 ms: 1.03x faster                                                   |
| html5lib                   | 33.0 ms                                                | 31.9 ms: 1.03x faster                                                  |
| pathlib                    | 23.2 ms                                                | 22.7 ms: 1.02x faster                                                  |
| fannkuch                   | 240 ms                                                 | 235 ms: 1.02x faster                                                   |
| go                         | 105 ms                                                 | 103 ms: 1.02x faster                                                   |
| tomli_loads                | 1.27 sec                                               | 1.25 sec: 1.02x faster                                                 |
| regex_compile              | 72.8 ms                                                | 72.7 ms: 1.00x faster                                                  |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.00x slower                                                   |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| meteor_contest             | 71.1 ms                                                | 71.5 ms: 1.01x slower                                                  |
| scimark_monte_carlo        | 43.5 ms                                                | 44.0 ms: 1.01x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.82 us: 1.01x slower                                                  |
| richards                   | 31.1 ms                                                | 31.5 ms: 1.01x slower                                                  |
| dulwich_log                | 28.6 ms                                                | 29.0 ms: 1.01x slower                                                  |
| xml_etree_parse            | 100 ms                                                 | 102 ms: 1.01x slower                                                   |
| nqueens                    | 55.9 ms                                                | 56.8 ms: 1.01x slower                                                  |
| pycparser                  | 659 ms                                                 | 672 ms: 1.02x slower                                                   |
| spectral_norm              | 65.7 ms                                                | 67.1 ms: 1.02x slower                                                  |
| chameleon                  | 4.30 ms                                                | 4.41 ms: 1.03x slower                                                  |
| bench_thread_pool          | 465 us                                                 | 478 us: 1.03x slower                                                   |
| coverage                   | 43.9 ms                                                | 45.1 ms: 1.03x slower                                                  |
| sympy_expand               | 229 ms                                                 | 236 ms: 1.03x slower                                                   |
| xml_etree_iterparse        | 68.3 ms                                                | 70.3 ms: 1.03x slower                                                  |
| nbody                      | 61.7 ms                                                | 63.6 ms: 1.03x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.92 ms: 1.04x slower                                                  |
| docutils                   | 1.43 sec                                               | 1.50 sec: 1.05x slower                                                 |
| regex_effbot               | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                  |
| django_template            | 20.1 ms                                                | 21.3 ms: 1.06x slower                                                  |
| json                       | 2.75 ms                                                | 2.93 ms: 1.07x slower                                                  |
| thrift                     | 410 us                                                 | 437 us: 1.07x slower                                                   |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.07x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 35.9 ms: 1.07x slower                                                  |
| unpickle_list              | 2.69 us                                                | 2.88 us: 1.07x slower                                                  |
| pickle                     | 6.98 us                                                | 7.49 us: 1.07x slower                                                  |
| scimark_fft                | 173 ms                                                 | 186 ms: 1.08x slower                                                   |
| mypy2                      | 372 ms                                                 | 404 ms: 1.08x slower                                                   |
| crypto_pyaes               | 47.5 ms                                                | 51.9 ms: 1.09x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.13 us: 1.10x slower                                                  |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| sqlglot_optimize           | 29.6 ms                                                | 32.7 ms: 1.10x slower                                                  |
| genshi_text                | 14.4 ms                                                | 16.0 ms: 1.11x slower                                                  |
| pyflate                    | 284 ms                                                 | 314 ms: 1.11x slower                                                   |
| pickle_list                | 2.70 us                                                | 2.99 us: 1.11x slower                                                  |
| 2to3                       | 154 ms                                                 | 172 ms: 1.11x slower                                                   |
| xml_etree_generate         | 45.8 ms                                                | 51.4 ms: 1.12x slower                                                  |
| regex_v8                   | 15.1 ms                                                | 17.3 ms: 1.15x slower                                                  |
| scimark_lu                 | 67.7 ms                                                | 78.7 ms: 1.16x slower                                                  |
| bench_mp_pool              | 41.0 ms                                                | 49.9 ms: 1.22x slower                                                  |
| sqlite_synth               | 1.26 us                                                | 1.57 us: 1.25x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 101 ms: 1.28x slower                                                   |
| create_gc_cycles           | 711 us                                                 | 909 us: 1.28x slower                                                   |
| flaskblogging              | 2.35 ms                                                | 3.25 ms: 1.38x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 39.5 ms: 1.39x slower                                                  |
| telco                      | 3.17 ms                                                | 4.55 ms: 1.43x slower                                                  |
| python_startup             | 10.8 ms                                                | 15.6 ms: 1.45x slower                                                  |
| python_startup_no_site     | 8.57 ms                                                | 12.7 ms: 1.48x slower                                                  |
| async_generators           | 192 ms                                                 | 296 ms: 1.54x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (5): tornado_http, asyncio_websockets, dask, gunicorn, aiohttp
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
Ignored benchmarks (8) of results/bm-20240604-3.13.0b1+-6725c78-JIT/bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 58.04% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.68x