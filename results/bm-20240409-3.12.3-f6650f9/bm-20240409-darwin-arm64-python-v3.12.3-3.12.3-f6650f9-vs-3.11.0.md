# Results vs. 3.11.0

- fork: python
- ref: v3.12.3
- machine: darwin-arm64
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.03x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 168 ms: 1.09x slower                                   |
| chameleon      | 4.30 ms                                                | 4.65 ms: 1.08x slower                                  |
| docutils       | 1.43 sec                                               | 1.49 sec: 1.04x slower                                 |
| tornado_http   | 69.1 ms                                                | 75.9 ms: 1.10x slower                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 326 ms: 1.08x faster                                   |
| async_tree_io_tg           | 724 ms                                                 | 677 ms: 1.07x faster                                   |
| async_tree_memoization     | 336 ms                                                 | 315 ms: 1.07x faster                                   |
| async_tree_none_tg         | 276 ms                                                 | 261 ms: 1.06x faster                                   |
| async_tree_none            | 282 ms                                                 | 269 ms: 1.05x faster                                   |
| async_tree_io              | 697 ms                                                 | 671 ms: 1.04x faster                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 534 ms: 1.03x faster                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 526 ms: 1.01x slower                                   |
| Geometric mean             | (ref)                                                  | 1.05x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 283 ms: 1.01x slower                                   |
| nbody          | 61.7 ms                                                | 67.4 ms: 1.09x slower                                  |
| float          | 50.8 ms                                                | 55.6 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 152 ms: 1.03x slower                                   |
| regex_compile  | 72.8 ms                                                | 77.6 ms: 1.07x slower                                  |
| regex_v8       | 15.1 ms                                                | 16.7 ms: 1.10x slower                                  |
| regex_effbot   | 2.43 ms                                                | 2.68 ms: 1.11x slower                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.26 ms: 1.20x faster                                  |
| unpickle_pure_python | 149 us                                                 | 149 us: 1.00x slower                                   |
| pickle_pure_python   | 191 us                                                 | 201 us: 1.05x slower                                   |
| pickle               | 6.98 us                                                | 7.35 us: 1.05x slower                                  |
| pickle_dict          | 17.1 us                                                | 18.1 us: 1.06x slower                                  |
| xml_etree_parse      | 100 ms                                                 | 107 ms: 1.07x slower                                   |
| pickle_list          | 2.70 us                                                | 2.89 us: 1.07x slower                                  |
| tomli_loads          | 1.27 sec                                               | 1.39 sec: 1.09x slower                                 |
| xml_etree_iterparse  | 68.3 ms                                                | 74.8 ms: 1.10x slower                                  |
| unpickle             | 8.29 us                                                | 9.38 us: 1.13x slower                                  |
| json_loads           | 15.3 us                                                | 17.4 us: 1.13x slower                                  |
| unpickle_list        | 2.69 us                                                | 3.08 us: 1.15x slower                                  |
| xml_etree_process    | 33.6 ms                                                | 39.8 ms: 1.18x slower                                  |
| xml_etree_generate   | 45.8 ms                                                | 56.2 ms: 1.23x slower                                  |
| Geometric mean       | (ref)                                                  | 1.08x slower                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 11.2 ms: 1.05x slower                                  |
| python_startup_no_site | 8.57 ms                                                | 8.97 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.05x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 7.93 ms                                                | 7.60 ms: 1.04x faster                                  |
| genshi_text     | 14.4 ms                                                | 15.4 ms: 1.07x slower                                  |
| genshi_xml      | 28.5 ms                                                | 31.7 ms: 1.11x slower                                  |
| django_template | 20.1 ms                                                | 22.4 ms: 1.11x slower                                  |
| Geometric mean  | (ref)                                                  | 1.06x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 73.5 us: 4.09x faster                                  |
| asyncio_tcp                | 643 ms                                                 | 408 ms: 1.58x faster                                   |
| pylint                     | 253 ms                                                 | 175 ms: 1.45x faster                                   |
| comprehensions             | 14.4 us                                                | 11.7 us: 1.24x faster                                  |
| json_dumps                 | 7.53 ms                                                | 6.26 ms: 1.20x faster                                  |
| coverage                   | 43.9 ms                                                | 39.1 ms: 1.12x faster                                  |
| chaos                      | 47.4 ms                                                | 42.8 ms: 1.11x faster                                  |
| sympy_sum                  | 80.2 ms                                                | 74.2 ms: 1.08x faster                                  |
| async_tree_memoization_tg  | 352 ms                                                 | 326 ms: 1.08x faster                                   |
| async_tree_io_tg           | 724 ms                                                 | 677 ms: 1.07x faster                                   |
| async_tree_memoization     | 336 ms                                                 | 315 ms: 1.07x faster                                   |
| async_tree_none_tg         | 276 ms                                                 | 261 ms: 1.06x faster                                   |
| async_tree_none            | 282 ms                                                 | 269 ms: 1.05x faster                                   |
| sqlglot_parse              | 890 us                                                 | 851 us: 1.05x faster                                   |
| mako                       | 7.93 ms                                                | 7.60 ms: 1.04x faster                                  |
| sqlalchemy_imperative      | 6.98 ms                                                | 6.71 ms: 1.04x faster                                  |
| async_tree_io              | 697 ms                                                 | 671 ms: 1.04x faster                                   |
| go                         | 105 ms                                                 | 102 ms: 1.04x faster                                   |
| richards_super             | 37.3 ms                                                | 36.1 ms: 1.03x faster                                  |
| sympy_integrate            | 11.3 ms                                                | 10.9 ms: 1.03x faster                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 534 ms: 1.03x faster                                   |
| deltablue                  | 2.75 ms                                                | 2.67 ms: 1.03x faster                                  |
| sqlglot_transpile          | 1.05 ms                                                | 1.02 ms: 1.03x faster                                  |
| create_gc_cycles           | 711 us                                                 | 695 us: 1.02x faster                                   |
| sympy_str                  | 144 ms                                                 | 141 ms: 1.02x faster                                   |
| hexiom                     | 4.58 ms                                                | 4.55 ms: 1.01x faster                                  |
| unpickle_pure_python       | 149 us                                                 | 149 us: 1.00x slower                                   |
| gc_traversal               | 2.38 ms                                                | 2.40 ms: 1.01x slower                                  |
| generators                 | 30.3 ms                                                | 30.5 ms: 1.01x slower                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.41 sec: 1.01x slower                                 |
| pidigits                   | 280 ms                                                 | 283 ms: 1.01x slower                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 526 ms: 1.01x slower                                   |
| raytrace                   | 206 ms                                                 | 211 ms: 1.02x slower                                   |
| dulwich_log                | 28.6 ms                                                | 29.3 ms: 1.02x slower                                  |
| regex_dna                  | 148 ms                                                 | 152 ms: 1.03x slower                                   |
| meteor_contest             | 71.1 ms                                                | 73.1 ms: 1.03x slower                                  |
| richards                   | 31.1 ms                                                | 32.0 ms: 1.03x slower                                  |
| pycparser                  | 659 ms                                                 | 681 ms: 1.03x slower                                   |
| pprint_pformat             | 979 ms                                                 | 1.01 sec: 1.03x slower                                 |
| docutils                   | 1.43 sec                                               | 1.49 sec: 1.04x slower                                 |
| fannkuch                   | 240 ms                                                 | 250 ms: 1.04x slower                                   |
| python_startup             | 10.8 ms                                                | 11.2 ms: 1.05x slower                                  |
| python_startup_no_site     | 8.57 ms                                                | 8.97 ms: 1.05x slower                                  |
| scimark_monte_carlo        | 43.5 ms                                                | 45.6 ms: 1.05x slower                                  |
| pprint_safe_repr           | 478 ms                                                 | 502 ms: 1.05x slower                                   |
| sympy_expand               | 229 ms                                                 | 241 ms: 1.05x slower                                   |
| pickle_pure_python         | 191 us                                                 | 201 us: 1.05x slower                                   |
| pickle                     | 6.98 us                                                | 7.35 us: 1.05x slower                                  |
| sqlalchemy_declarative     | 59.3 ms                                                | 62.5 ms: 1.05x slower                                  |
| pickle_dict                | 17.1 us                                                | 18.1 us: 1.06x slower                                  |
| regex_compile              | 72.8 ms                                                | 77.6 ms: 1.07x slower                                  |
| mdp                        | 1.48 sec                                               | 1.58 sec: 1.07x slower                                 |
| genshi_text                | 14.4 ms                                                | 15.4 ms: 1.07x slower                                  |
| xml_etree_parse            | 100 ms                                                 | 107 ms: 1.07x slower                                   |
| deepcopy_memo              | 25.7 us                                                | 27.5 us: 1.07x slower                                  |
| bench_thread_pool          | 465 us                                                 | 498 us: 1.07x slower                                   |
| deepcopy                   | 215 us                                                 | 230 us: 1.07x slower                                   |
| pickle_list                | 2.70 us                                                | 2.89 us: 1.07x slower                                  |
| bench_mp_pool              | 41.0 ms                                                | 44.0 ms: 1.07x slower                                  |
| chameleon                  | 4.30 ms                                                | 4.65 ms: 1.08x slower                                  |
| logging_format             | 3.67 us                                                | 4.00 us: 1.09x slower                                  |
| logging_simple             | 3.41 us                                                | 3.71 us: 1.09x slower                                  |
| pathlib                    | 23.2 ms                                                | 25.3 ms: 1.09x slower                                  |
| 2to3                       | 154 ms                                                 | 168 ms: 1.09x slower                                   |
| tomli_loads                | 1.27 sec                                               | 1.39 sec: 1.09x slower                                 |
| nbody                      | 61.7 ms                                                | 67.4 ms: 1.09x slower                                  |
| crypto_pyaes               | 47.5 ms                                                | 51.9 ms: 1.09x slower                                  |
| float                      | 50.8 ms                                                | 55.6 ms: 1.09x slower                                  |
| xml_etree_iterparse        | 68.3 ms                                                | 74.8 ms: 1.10x slower                                  |
| coroutines                 | 17.2 ms                                                | 18.8 ms: 1.10x slower                                  |
| tornado_http               | 69.1 ms                                                | 75.9 ms: 1.10x slower                                  |
| regex_v8                   | 15.1 ms                                                | 16.7 ms: 1.10x slower                                  |
| regex_effbot               | 2.43 ms                                                | 2.68 ms: 1.11x slower                                  |
| scimark_lu                 | 67.7 ms                                                | 75.0 ms: 1.11x slower                                  |
| json                       | 2.75 ms                                                | 3.06 ms: 1.11x slower                                  |
| genshi_xml                 | 28.5 ms                                                | 31.7 ms: 1.11x slower                                  |
| django_template            | 20.1 ms                                                | 22.4 ms: 1.11x slower                                  |
| scimark_sor                | 79.2 ms                                                | 88.2 ms: 1.11x slower                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.15 ms: 1.12x slower                                  |
| pyflate                    | 284 ms                                                 | 318 ms: 1.12x slower                                   |
| nqueens                    | 55.9 ms                                                | 63.2 ms: 1.13x slower                                  |
| unpickle                   | 8.29 us                                                | 9.38 us: 1.13x slower                                  |
| json_loads                 | 15.3 us                                                | 17.4 us: 1.13x slower                                  |
| deepcopy_reduce            | 1.79 us                                                | 2.03 us: 1.13x slower                                  |
| scimark_fft                | 173 ms                                                 | 198 ms: 1.15x slower                                   |
| unpickle_list              | 2.69 us                                                | 3.08 us: 1.15x slower                                  |
| sqlglot_normalize          | 162 ms                                                 | 186 ms: 1.15x slower                                   |
| sqlglot_optimize           | 29.6 ms                                                | 34.1 ms: 1.15x slower                                  |
| spectral_norm              | 65.7 ms                                                | 76.2 ms: 1.16x slower                                  |
| thrift                     | 410 us                                                 | 479 us: 1.17x slower                                   |
| logging_silent             | 66.5 ns                                                | 78.7 ns: 1.18x slower                                  |
| xml_etree_process          | 33.6 ms                                                | 39.8 ms: 1.18x slower                                  |
| telco                      | 3.17 ms                                                | 3.76 ms: 1.19x slower                                  |
| xml_etree_generate         | 45.8 ms                                                | 56.2 ms: 1.23x slower                                  |
| mypy2                      | 372 ms                                                 | 457 ms: 1.23x slower                                   |
| sqlite_synth               | 1.26 us                                                | 1.58 us: 1.26x slower                                  |
| async_generators           | 192 ms                                                 | 301 ms: 1.57x slower                                   |
| Geometric mean             | (ref)                                                  | 1.03x slower                                           |

Benchmark hidden because not significant (5): gunicorn, aiohttp, html5lib, asyncio_websockets, dask
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, unpack_sequence
Ignored benchmarks (8) of results/bm-20240409-3.12.3-f6650f9/bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.00x