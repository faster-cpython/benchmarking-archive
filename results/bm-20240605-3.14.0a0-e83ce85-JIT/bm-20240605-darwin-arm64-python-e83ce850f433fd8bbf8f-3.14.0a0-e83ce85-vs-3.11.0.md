# Results vs. 3.11.0

- fork: python
- ref: e83ce850f433fd8bbf8f
- machine: darwin-arm64
- commit hash: e83ce85
- commit date: 2024-06-05
- overall geometric mean: 1.02x faster
- HPT reliability: 63.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.64x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 170 ms: 1.10x slower                                                  |
| docutils       | 1.43 sec                                               | 1.50 sec: 1.05x slower                                                |
| html5lib       | 33.0 ms                                                | 30.9 ms: 1.07x faster                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 238 ms: 1.48x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 196 ms: 1.41x faster                                                  |
| async_tree_none            | 282 ms                                                 | 215 ms: 1.31x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 555 ms: 1.30x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 263 ms: 1.28x faster                                                  |
| async_tree_io              | 697 ms                                                 | 571 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 452 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 473 ms: 1.10x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 47.7 ms: 1.07x faster                                                 |
| pidigits       | 280 ms                                                 | 281 ms: 1.00x slower                                                  |
| nbody          | 61.7 ms                                                | 64.0 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 72.4 ms: 1.01x faster                                                 |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| regex_effbot   | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                 |
| regex_v8       | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.32 ms: 1.19x faster                                                 |
| unpickle_pure_python | 149 us                                                 | 132 us: 1.13x faster                                                  |
| pickle_pure_python   | 191 us                                                 | 172 us: 1.12x faster                                                  |
| tomli_loads          | 1.27 sec                                               | 1.25 sec: 1.02x faster                                                |
| xml_etree_iterparse  | 68.3 ms                                                | 70.1 ms: 1.03x slower                                                 |
| xml_etree_parse      | 100 ms                                                 | 105 ms: 1.05x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 35.6 ms: 1.06x slower                                                 |
| unpickle_list        | 2.69 us                                                | 2.85 us: 1.06x slower                                                 |
| pickle               | 6.98 us                                                | 7.45 us: 1.07x slower                                                 |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.07x slower                                                 |
| pickle_list          | 2.70 us                                                | 2.94 us: 1.09x slower                                                 |
| json_loads           | 15.3 us                                                | 17.0 us: 1.10x slower                                                 |
| xml_etree_generate   | 45.8 ms                                                | 51.1 ms: 1.12x slower                                                 |
| unpickle             | 8.29 us                                                | 9.30 us: 1.12x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 15.4 ms: 1.43x slower                                                 |
| python_startup_no_site | 8.57 ms                                                | 12.7 ms: 1.48x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.36 ms: 1.25x faster                                                 |
| django_template | 20.1 ms                                                | 21.5 ms: 1.07x slower                                                 |
| genshi_text     | 14.4 ms                                                | 16.9 ms: 1.18x slower                                                 |
| genshi_xml      | 28.5 ms                                                | 39.3 ms: 1.38x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.09x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 95.3 us: 3.16x faster                                                 |
| async_tree_memoization_tg  | 352 ms                                                 | 238 ms: 1.48x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 196 ms: 1.41x faster                                                  |
| asyncio_tcp                | 643 ms                                                 | 457 ms: 1.41x faster                                                  |
| pylint                     | 253 ms                                                 | 183 ms: 1.38x faster                                                  |
| async_tree_none            | 282 ms                                                 | 215 ms: 1.31x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 555 ms: 1.30x faster                                                  |
| generators                 | 30.3 ms                                                | 23.5 ms: 1.29x faster                                                 |
| async_tree_memoization     | 336 ms                                                 | 263 ms: 1.28x faster                                                  |
| raytrace                   | 206 ms                                                 | 164 ms: 1.25x faster                                                  |
| mako                       | 7.93 ms                                                | 6.36 ms: 1.25x faster                                                 |
| async_tree_io              | 697 ms                                                 | 571 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 452 ms: 1.22x faster                                                  |
| deepcopy_memo              | 25.7 us                                                | 21.3 us: 1.21x faster                                                 |
| chaos                      | 47.4 ms                                                | 39.7 ms: 1.19x faster                                                 |
| json_dumps                 | 7.53 ms                                                | 6.32 ms: 1.19x faster                                                 |
| comprehensions             | 14.4 us                                                | 12.3 us: 1.17x faster                                                 |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.23 sec: 1.13x faster                                                |
| unpickle_pure_python       | 149 us                                                 | 132 us: 1.13x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 172 us: 1.12x faster                                                  |
| deltablue                  | 2.75 ms                                                | 2.47 ms: 1.11x faster                                                 |
| sympy_sum                  | 80.2 ms                                                | 72.6 ms: 1.10x faster                                                 |
| logging_simple             | 3.41 us                                                | 3.10 us: 1.10x faster                                                 |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 473 ms: 1.10x faster                                                  |
| coroutines                 | 17.2 ms                                                | 15.8 ms: 1.08x faster                                                 |
| sqlglot_parse              | 890 us                                                 | 830 us: 1.07x faster                                                  |
| logging_format             | 3.67 us                                                | 3.44 us: 1.07x faster                                                 |
| html5lib                   | 33.0 ms                                                | 30.9 ms: 1.07x faster                                                 |
| float                      | 50.8 ms                                                | 47.7 ms: 1.07x faster                                                 |
| pathlib                    | 23.2 ms                                                | 21.9 ms: 1.06x faster                                                 |
| deepcopy                   | 215 us                                                 | 206 us: 1.05x faster                                                  |
| richards_super             | 37.3 ms                                                | 35.6 ms: 1.05x faster                                                 |
| sqlglot_transpile          | 1.05 ms                                                | 1.01 ms: 1.04x faster                                                 |
| logging_silent             | 66.5 ns                                                | 63.8 ns: 1.04x faster                                                 |
| pprint_safe_repr           | 478 ms                                                 | 460 ms: 1.04x faster                                                  |
| hexiom                     | 4.58 ms                                                | 4.41 ms: 1.04x faster                                                 |
| sympy_str                  | 144 ms                                                 | 139 ms: 1.04x faster                                                  |
| pprint_pformat             | 979 ms                                                 | 947 ms: 1.03x faster                                                  |
| sympy_integrate            | 11.3 ms                                                | 10.9 ms: 1.03x faster                                                 |
| go                         | 105 ms                                                 | 102 ms: 1.03x faster                                                  |
| mdp                        | 1.48 sec                                               | 1.44 sec: 1.03x faster                                                |
| tomli_loads                | 1.27 sec                                               | 1.25 sec: 1.02x faster                                                |
| regex_compile              | 72.8 ms                                                | 72.4 ms: 1.01x faster                                                 |
| fannkuch                   | 240 ms                                                 | 239 ms: 1.00x faster                                                  |
| asyncio_websockets         | 408 ms                                                 | 409 ms: 1.00x slower                                                  |
| pidigits                   | 280 ms                                                 | 281 ms: 1.00x slower                                                  |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| dask                       | 219 ms                                                 | 222 ms: 1.01x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.82 us: 1.01x slower                                                 |
| richards                   | 31.1 ms                                                | 31.6 ms: 1.02x slower                                                 |
| meteor_contest             | 71.1 ms                                                | 72.5 ms: 1.02x slower                                                 |
| scimark_monte_carlo        | 43.5 ms                                                | 44.5 ms: 1.02x slower                                                 |
| spectral_norm              | 65.7 ms                                                | 67.3 ms: 1.02x slower                                                 |
| xml_etree_iterparse        | 68.3 ms                                                | 70.1 ms: 1.03x slower                                                 |
| pycparser                  | 659 ms                                                 | 677 ms: 1.03x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.47 ms: 1.04x slower                                                 |
| nbody                      | 61.7 ms                                                | 64.0 ms: 1.04x slower                                                 |
| bench_thread_pool          | 465 us                                                 | 483 us: 1.04x slower                                                  |
| coverage                   | 43.9 ms                                                | 45.6 ms: 1.04x slower                                                 |
| sympy_expand               | 229 ms                                                 | 239 ms: 1.04x slower                                                  |
| xml_etree_parse            | 100 ms                                                 | 105 ms: 1.05x slower                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.95 ms: 1.05x slower                                                 |
| docutils                   | 1.43 sec                                               | 1.50 sec: 1.05x slower                                                |
| nqueens                    | 55.9 ms                                                | 58.9 ms: 1.05x slower                                                 |
| regex_effbot               | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                 |
| thrift                     | 410 us                                                 | 434 us: 1.06x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 35.6 ms: 1.06x slower                                                 |
| unpickle_list              | 2.69 us                                                | 2.85 us: 1.06x slower                                                 |
| json                       | 2.75 ms                                                | 2.93 ms: 1.06x slower                                                 |
| pickle                     | 6.98 us                                                | 7.45 us: 1.07x slower                                                 |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.07x slower                                                 |
| django_template            | 20.1 ms                                                | 21.5 ms: 1.07x slower                                                 |
| scimark_fft                | 173 ms                                                 | 185 ms: 1.07x slower                                                  |
| pickle_list                | 2.70 us                                                | 2.94 us: 1.09x slower                                                 |
| crypto_pyaes               | 47.5 ms                                                | 51.8 ms: 1.09x slower                                                 |
| 2to3                       | 154 ms                                                 | 170 ms: 1.10x slower                                                  |
| json_loads                 | 15.3 us                                                | 17.0 us: 1.10x slower                                                 |
| pyflate                    | 284 ms                                                 | 314 ms: 1.11x slower                                                  |
| xml_etree_generate         | 45.8 ms                                                | 51.1 ms: 1.12x slower                                                 |
| sqlglot_optimize           | 29.6 ms                                                | 33.2 ms: 1.12x slower                                                 |
| unpickle                   | 8.29 us                                                | 9.30 us: 1.12x slower                                                 |
| regex_v8                   | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                 |
| scimark_lu                 | 67.7 ms                                                | 79.1 ms: 1.17x slower                                                 |
| genshi_text                | 14.4 ms                                                | 16.9 ms: 1.18x slower                                                 |
| bench_mp_pool              | 41.0 ms                                                | 49.4 ms: 1.21x slower                                                 |
| sqlite_synth               | 1.26 us                                                | 1.56 us: 1.25x slower                                                 |
| scimark_sor                | 79.2 ms                                                | 102 ms: 1.28x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 914 us: 1.29x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 39.3 ms: 1.38x slower                                                 |
| telco                      | 3.17 ms                                                | 4.47 ms: 1.41x slower                                                 |
| python_startup             | 10.8 ms                                                | 15.4 ms: 1.43x slower                                                 |
| python_startup_no_site     | 8.57 ms                                                | 12.7 ms: 1.48x slower                                                 |
| async_generators           | 192 ms                                                 | 289 ms: 1.51x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): tornado_http
Ignored benchmarks (10) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
Ignored benchmarks (8) of results/bm-20240605-3.14.0a0-e83ce85-JIT/bm-20240605-darwin-arm64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 63.92% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.64x