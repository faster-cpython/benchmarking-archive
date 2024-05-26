# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: darwin-arm64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.01x faster
- HPT reliability: 60.24%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.59x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 172 ms: 1.11x slower                                                  |
| chameleon      | 4.30 ms                                                | 4.42 ms: 1.03x slower                                                 |
| docutils       | 1.43 sec                                               | 1.51 sec: 1.05x slower                                                |
| html5lib       | 33.0 ms                                                | 31.0 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 241 ms: 1.46x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 198 ms: 1.39x faster                                                  |
| async_tree_none            | 282 ms                                                 | 216 ms: 1.31x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 562 ms: 1.29x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 266 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 449 ms: 1.22x faster                                                  |
| async_tree_io              | 697 ms                                                 | 580 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 473 ms: 1.10x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 47.3 ms: 1.08x faster                                                 |
| pidigits       | 280 ms                                                 | 282 ms: 1.00x slower                                                  |
| nbody          | 61.7 ms                                                | 63.7 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 72.4 ms: 1.01x faster                                                 |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| regex_effbot   | 2.43 ms                                                | 2.57 ms: 1.06x slower                                                 |
| regex_v8       | 15.1 ms                                                | 17.5 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.19 ms: 1.22x faster                                                 |
| unpickle_pure_python | 149 us                                                 | 132 us: 1.13x faster                                                  |
| pickle_pure_python   | 191 us                                                 | 172 us: 1.11x faster                                                  |
| tomli_loads          | 1.27 sec                                               | 1.26 sec: 1.01x faster                                                |
| xml_etree_iterparse  | 68.3 ms                                                | 70.2 ms: 1.03x slower                                                 |
| xml_etree_parse      | 100 ms                                                 | 104 ms: 1.04x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 35.7 ms: 1.06x slower                                                 |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.06x slower                                                 |
| pickle               | 6.98 us                                                | 7.44 us: 1.07x slower                                                 |
| unpickle_list        | 2.69 us                                                | 2.89 us: 1.08x slower                                                 |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                                 |
| pickle_list          | 2.70 us                                                | 2.98 us: 1.11x slower                                                 |
| xml_etree_generate   | 45.8 ms                                                | 51.2 ms: 1.12x slower                                                 |
| unpickle             | 8.29 us                                                | 9.27 us: 1.12x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 15.9 ms: 1.48x slower                                                 |
| python_startup_no_site | 8.57 ms                                                | 13.3 ms: 1.55x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.51x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.37 ms: 1.25x faster                                                 |
| django_template | 20.1 ms                                                | 21.5 ms: 1.07x slower                                                 |
| genshi_text     | 14.4 ms                                                | 16.3 ms: 1.13x slower                                                 |
| genshi_xml      | 28.5 ms                                                | 39.3 ms: 1.38x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.08x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 95.5 us: 3.15x faster                                                 |
| async_tree_memoization_tg  | 352 ms                                                 | 241 ms: 1.46x faster                                                  |
| asyncio_tcp                | 643 ms                                                 | 440 ms: 1.46x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 198 ms: 1.39x faster                                                  |
| pylint                     | 253 ms                                                 | 182 ms: 1.39x faster                                                  |
| generators                 | 30.3 ms                                                | 23.0 ms: 1.32x faster                                                 |
| async_tree_none            | 282 ms                                                 | 216 ms: 1.31x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 562 ms: 1.29x faster                                                  |
| raytrace                   | 206 ms                                                 | 162 ms: 1.27x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 266 ms: 1.26x faster                                                  |
| mako                       | 7.93 ms                                                | 6.37 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 449 ms: 1.22x faster                                                  |
| json_dumps                 | 7.53 ms                                                | 6.19 ms: 1.22x faster                                                 |
| chaos                      | 47.4 ms                                                | 39.2 ms: 1.21x faster                                                 |
| async_tree_io              | 697 ms                                                 | 580 ms: 1.20x faster                                                  |
| deepcopy_memo              | 25.7 us                                                | 21.6 us: 1.19x faster                                                 |
| comprehensions             | 14.4 us                                                | 12.3 us: 1.18x faster                                                 |
| unpickle_pure_python       | 149 us                                                 | 132 us: 1.13x faster                                                  |
| deltablue                  | 2.75 ms                                                | 2.46 ms: 1.12x faster                                                 |
| logging_simple             | 3.41 us                                                | 3.05 us: 1.12x faster                                                 |
| pickle_pure_python         | 191 us                                                 | 172 us: 1.11x faster                                                  |
| logging_format             | 3.67 us                                                | 3.35 us: 1.10x faster                                                 |
| sympy_sum                  | 80.2 ms                                                | 73.1 ms: 1.10x faster                                                 |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 473 ms: 1.10x faster                                                  |
| sqlglot_parse              | 890 us                                                 | 826 us: 1.08x faster                                                  |
| float                      | 50.8 ms                                                | 47.3 ms: 1.08x faster                                                 |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.30 sec: 1.07x faster                                                |
| coroutines                 | 17.2 ms                                                | 16.0 ms: 1.07x faster                                                 |
| html5lib                   | 33.0 ms                                                | 31.0 ms: 1.06x faster                                                 |
| logging_silent             | 66.5 ns                                                | 62.9 ns: 1.06x faster                                                 |
| sqlglot_transpile          | 1.05 ms                                                | 1.00 ms: 1.05x faster                                                 |
| richards_super             | 37.3 ms                                                | 35.6 ms: 1.05x faster                                                 |
| sympy_str                  | 144 ms                                                 | 137 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 478 ms                                                 | 457 ms: 1.05x faster                                                  |
| deepcopy                   | 215 us                                                 | 207 us: 1.04x faster                                                  |
| pprint_pformat             | 979 ms                                                 | 940 ms: 1.04x faster                                                  |
| hexiom                     | 4.58 ms                                                | 4.43 ms: 1.03x faster                                                 |
| go                         | 105 ms                                                 | 102 ms: 1.03x faster                                                  |
| sympy_integrate            | 11.3 ms                                                | 10.9 ms: 1.03x faster                                                 |
| pathlib                    | 23.2 ms                                                | 22.5 ms: 1.03x faster                                                 |
| tomli_loads                | 1.27 sec                                               | 1.26 sec: 1.01x faster                                                |
| regex_compile              | 72.8 ms                                                | 72.4 ms: 1.01x faster                                                 |
| asyncio_websockets         | 408 ms                                                 | 409 ms: 1.00x slower                                                  |
| pidigits                   | 280 ms                                                 | 282 ms: 1.00x slower                                                  |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.81 us: 1.01x slower                                                 |
| scimark_monte_carlo        | 43.5 ms                                                | 44.3 ms: 1.02x slower                                                 |
| mdp                        | 1.48 sec                                               | 1.51 sec: 1.02x slower                                                |
| fannkuch                   | 240 ms                                                 | 244 ms: 1.02x slower                                                  |
| meteor_contest             | 71.1 ms                                                | 72.5 ms: 1.02x slower                                                 |
| richards                   | 31.1 ms                                                | 31.7 ms: 1.02x slower                                                 |
| dask                       | 219 ms                                                 | 224 ms: 1.02x slower                                                  |
| spectral_norm              | 65.7 ms                                                | 67.3 ms: 1.02x slower                                                 |
| nqueens                    | 55.9 ms                                                | 57.4 ms: 1.03x slower                                                 |
| xml_etree_iterparse        | 68.3 ms                                                | 70.2 ms: 1.03x slower                                                 |
| chameleon                  | 4.30 ms                                                | 4.42 ms: 1.03x slower                                                 |
| bench_thread_pool          | 465 us                                                 | 480 us: 1.03x slower                                                  |
| nbody                      | 61.7 ms                                                | 63.7 ms: 1.03x slower                                                 |
| sympy_expand               | 229 ms                                                 | 237 ms: 1.03x slower                                                  |
| coverage                   | 43.9 ms                                                | 45.5 ms: 1.04x slower                                                 |
| gc_traversal               | 2.38 ms                                                | 2.47 ms: 1.04x slower                                                 |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.92 ms: 1.04x slower                                                 |
| xml_etree_parse            | 100 ms                                                 | 104 ms: 1.04x slower                                                  |
| thrift                     | 410 us                                                 | 433 us: 1.05x slower                                                  |
| docutils                   | 1.43 sec                                               | 1.51 sec: 1.05x slower                                                |
| json                       | 2.75 ms                                                | 2.91 ms: 1.06x slower                                                 |
| regex_effbot               | 2.43 ms                                                | 2.57 ms: 1.06x slower                                                 |
| xml_etree_process          | 33.6 ms                                                | 35.7 ms: 1.06x slower                                                 |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.06x slower                                                 |
| pickle                     | 6.98 us                                                | 7.44 us: 1.07x slower                                                 |
| scimark_fft                | 173 ms                                                 | 184 ms: 1.07x slower                                                  |
| django_template            | 20.1 ms                                                | 21.5 ms: 1.07x slower                                                 |
| unpickle_list              | 2.69 us                                                | 2.89 us: 1.08x slower                                                 |
| crypto_pyaes               | 47.5 ms                                                | 52.0 ms: 1.10x slower                                                 |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                                 |
| pickle_list                | 2.70 us                                                | 2.98 us: 1.11x slower                                                 |
| pyflate                    | 284 ms                                                 | 315 ms: 1.11x slower                                                  |
| sqlglot_optimize           | 29.6 ms                                                | 32.9 ms: 1.11x slower                                                 |
| 2to3                       | 154 ms                                                 | 172 ms: 1.11x slower                                                  |
| xml_etree_generate         | 45.8 ms                                                | 51.2 ms: 1.12x slower                                                 |
| unpickle                   | 8.29 us                                                | 9.27 us: 1.12x slower                                                 |
| genshi_text                | 14.4 ms                                                | 16.3 ms: 1.13x slower                                                 |
| scimark_lu                 | 67.7 ms                                                | 78.1 ms: 1.15x slower                                                 |
| regex_v8                   | 15.1 ms                                                | 17.5 ms: 1.16x slower                                                 |
| bench_mp_pool              | 41.0 ms                                                | 49.9 ms: 1.22x slower                                                 |
| sqlite_synth               | 1.26 us                                                | 1.56 us: 1.24x slower                                                 |
| scimark_sor                | 79.2 ms                                                | 100 ms: 1.26x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 908 us: 1.28x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 39.3 ms: 1.38x slower                                                 |
| telco                      | 3.17 ms                                                | 4.59 ms: 1.45x slower                                                 |
| python_startup             | 10.8 ms                                                | 15.9 ms: 1.48x slower                                                 |
| flaskblogging              | 2.35 ms                                                | 3.57 ms: 1.52x slower                                                 |
| async_generators           | 192 ms                                                 | 294 ms: 1.53x slower                                                  |
| python_startup_no_site     | 8.57 ms                                                | 13.3 ms: 1.55x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): tornado_http, pycparser
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dulwich_log, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
Ignored benchmarks (8) of results/bm-20240525-3.14.0a0-e418fc3-JIT/bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 60.24% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.59x