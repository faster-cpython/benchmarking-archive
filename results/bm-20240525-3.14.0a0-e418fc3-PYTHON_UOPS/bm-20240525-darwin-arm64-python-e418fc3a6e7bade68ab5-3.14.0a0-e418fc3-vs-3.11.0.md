# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: darwin-arm64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.10x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.73x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 182 ms: 1.18x slower                                                  |
| chameleon      | 4.30 ms                                                | 4.99 ms: 1.16x slower                                                 |
| docutils       | 1.43 sec                                               | 1.68 sec: 1.17x slower                                                |
| Geometric mean | (ref)                                                  | 1.11x slower                                                          |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 261 ms: 1.35x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 207 ms: 1.33x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 565 ms: 1.28x faster                                                  |
| async_tree_none            | 282 ms                                                 | 226 ms: 1.24x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 279 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 459 ms: 1.20x faster                                                  |
| async_tree_io              | 697 ms                                                 | 587 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 488 ms: 1.06x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.23x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 283 ms: 1.01x slower                                                  |
| float          | 50.8 ms                                                | 61.3 ms: 1.21x slower                                                 |
| nbody          | 61.7 ms                                                | 76.1 ms: 1.23x slower                                                 |
| Geometric mean | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| regex_effbot   | 2.43 ms                                                | 2.59 ms: 1.07x slower                                                 |
| regex_v8       | 15.1 ms                                                | 17.6 ms: 1.16x slower                                                 |
| regex_compile  | 72.8 ms                                                | 96.5 ms: 1.32x slower                                                 |
| Geometric mean | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.62 ms: 1.14x faster                                                 |
| xml_etree_parse      | 100 ms                                                 | 106 ms: 1.06x slower                                                  |
| pickle               | 6.98 us                                                | 7.41 us: 1.06x slower                                                 |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.07x slower                                                 |
| unpickle_list        | 2.69 us                                                | 2.90 us: 1.08x slower                                                 |
| pickle_list          | 2.70 us                                                | 2.95 us: 1.09x slower                                                 |
| json_loads           | 15.3 us                                                | 17.0 us: 1.11x slower                                                 |
| unpickle             | 8.29 us                                                | 9.28 us: 1.12x slower                                                 |
| xml_etree_iterparse  | 68.3 ms                                                | 76.6 ms: 1.12x slower                                                 |
| pickle_pure_python   | 191 us                                                 | 228 us: 1.19x slower                                                  |
| unpickle_pure_python | 149 us                                                 | 179 us: 1.21x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 41.4 ms: 1.23x slower                                                 |
| xml_etree_generate   | 45.8 ms                                                | 59.0 ms: 1.29x slower                                                 |
| tomli_loads          | 1.27 sec                                               | 1.65 sec: 1.30x slower                                                |
| Geometric mean       | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 14.6 ms: 1.36x slower                                                 |
| python_startup_no_site | 8.57 ms                                                | 12.0 ms: 1.40x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.38x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 9.12 ms: 1.15x slower                                                 |
| django_template | 20.1 ms                                                | 24.1 ms: 1.20x slower                                                 |
| genshi_text     | 14.4 ms                                                | 17.5 ms: 1.21x slower                                                 |
| genshi_xml      | 28.5 ms                                                | 36.4 ms: 1.28x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.21x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 109 us: 2.76x faster                                                  |
| asyncio_tcp                | 643 ms                                                 | 406 ms: 1.58x faster                                                  |
| async_tree_memoization_tg  | 352 ms                                                 | 261 ms: 1.35x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 207 ms: 1.33x faster                                                  |
| pylint                     | 253 ms                                                 | 194 ms: 1.30x faster                                                  |
| generators                 | 30.3 ms                                                | 23.4 ms: 1.30x faster                                                 |
| async_tree_io_tg           | 724 ms                                                 | 565 ms: 1.28x faster                                                  |
| async_tree_none            | 282 ms                                                 | 226 ms: 1.24x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 279 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 459 ms: 1.20x faster                                                  |
| async_tree_io              | 697 ms                                                 | 587 ms: 1.19x faster                                                  |
| raytrace                   | 206 ms                                                 | 178 ms: 1.15x faster                                                  |
| json_dumps                 | 7.53 ms                                                | 6.62 ms: 1.14x faster                                                 |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.29 sec: 1.08x faster                                                |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 488 ms: 1.06x faster                                                  |
| logging_simple             | 3.41 us                                                | 3.25 us: 1.05x faster                                                 |
| coroutines                 | 17.2 ms                                                | 16.6 ms: 1.04x faster                                                 |
| logging_format             | 3.67 us                                                | 3.56 us: 1.03x faster                                                 |
| chaos                      | 47.4 ms                                                | 46.8 ms: 1.01x faster                                                 |
| pathlib                    | 23.2 ms                                                | 23.0 ms: 1.01x faster                                                 |
| pidigits                   | 280 ms                                                 | 283 ms: 1.01x slower                                                  |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.47 ms: 1.04x slower                                                 |
| dask                       | 219 ms                                                 | 228 ms: 1.04x slower                                                  |
| coverage                   | 43.9 ms                                                | 46.2 ms: 1.05x slower                                                 |
| xml_etree_parse            | 100 ms                                                 | 106 ms: 1.06x slower                                                  |
| pickle                     | 6.98 us                                                | 7.41 us: 1.06x slower                                                 |
| deltablue                  | 2.75 ms                                                | 2.93 ms: 1.07x slower                                                 |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.07x slower                                                 |
| regex_effbot               | 2.43 ms                                                | 2.59 ms: 1.07x slower                                                 |
| sqlglot_parse              | 890 us                                                 | 958 us: 1.08x slower                                                  |
| thrift                     | 410 us                                                 | 443 us: 1.08x slower                                                  |
| unpickle_list              | 2.69 us                                                | 2.90 us: 1.08x slower                                                 |
| json                       | 2.75 ms                                                | 2.98 ms: 1.08x slower                                                 |
| sympy_sum                  | 80.2 ms                                                | 87.2 ms: 1.09x slower                                                 |
| pickle_list                | 2.70 us                                                | 2.95 us: 1.09x slower                                                 |
| richards_super             | 37.3 ms                                                | 40.9 ms: 1.10x slower                                                 |
| sqlglot_transpile          | 1.05 ms                                                | 1.16 ms: 1.10x slower                                                 |
| json_loads                 | 15.3 us                                                | 17.0 us: 1.11x slower                                                 |
| pycparser                  | 659 ms                                                 | 731 ms: 1.11x slower                                                  |
| mdp                        | 1.48 sec                                               | 1.65 sec: 1.11x slower                                                |
| go                         | 105 ms                                                 | 117 ms: 1.11x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.28 us: 1.12x slower                                                 |
| xml_etree_iterparse        | 68.3 ms                                                | 76.6 ms: 1.12x slower                                                 |
| sympy_integrate            | 11.3 ms                                                | 12.7 ms: 1.13x slower                                                 |
| meteor_contest             | 71.1 ms                                                | 80.1 ms: 1.13x slower                                                 |
| bench_thread_pool          | 465 us                                                 | 533 us: 1.14x slower                                                  |
| mako                       | 7.93 ms                                                | 9.12 ms: 1.15x slower                                                 |
| sympy_str                  | 144 ms                                                 | 166 ms: 1.15x slower                                                  |
| bench_mp_pool              | 41.0 ms                                                | 47.5 ms: 1.16x slower                                                 |
| regex_v8                   | 15.1 ms                                                | 17.6 ms: 1.16x slower                                                 |
| chameleon                  | 4.30 ms                                                | 4.99 ms: 1.16x slower                                                 |
| sympy_expand               | 229 ms                                                 | 266 ms: 1.16x slower                                                  |
| deepcopy                   | 215 us                                                 | 253 us: 1.17x slower                                                  |
| docutils                   | 1.43 sec                                               | 1.68 sec: 1.17x slower                                                |
| 2to3                       | 154 ms                                                 | 182 ms: 1.18x slower                                                  |
| pickle_pure_python         | 191 us                                                 | 228 us: 1.19x slower                                                  |
| django_template            | 20.1 ms                                                | 24.1 ms: 1.20x slower                                                 |
| deepcopy_reduce            | 1.79 us                                                | 2.15 us: 1.20x slower                                                 |
| richards                   | 31.1 ms                                                | 37.3 ms: 1.20x slower                                                 |
| pprint_pformat             | 979 ms                                                 | 1.18 sec: 1.20x slower                                                |
| unpickle_pure_python       | 149 us                                                 | 179 us: 1.21x slower                                                  |
| pprint_safe_repr           | 478 ms                                                 | 576 ms: 1.21x slower                                                  |
| float                      | 50.8 ms                                                | 61.3 ms: 1.21x slower                                                 |
| comprehensions             | 14.4 us                                                | 17.5 us: 1.21x slower                                                 |
| genshi_text                | 14.4 ms                                                | 17.5 ms: 1.21x slower                                                 |
| xml_etree_process          | 33.6 ms                                                | 41.4 ms: 1.23x slower                                                 |
| nbody                      | 61.7 ms                                                | 76.1 ms: 1.23x slower                                                 |
| nqueens                    | 55.9 ms                                                | 69.1 ms: 1.24x slower                                                 |
| deepcopy_memo              | 25.7 us                                                | 32.6 us: 1.27x slower                                                 |
| sqlglot_optimize           | 29.6 ms                                                | 37.6 ms: 1.27x slower                                                 |
| create_gc_cycles           | 711 us                                                 | 905 us: 1.27x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 36.4 ms: 1.28x slower                                                 |
| sqlite_synth               | 1.26 us                                                | 1.61 us: 1.28x slower                                                 |
| xml_etree_generate         | 45.8 ms                                                | 59.0 ms: 1.29x slower                                                 |
| crypto_pyaes               | 47.5 ms                                                | 61.3 ms: 1.29x slower                                                 |
| scimark_fft                | 173 ms                                                 | 223 ms: 1.29x slower                                                  |
| tomli_loads                | 1.27 sec                                               | 1.65 sec: 1.30x slower                                                |
| hexiom                     | 4.58 ms                                                | 5.98 ms: 1.31x slower                                                 |
| regex_compile              | 72.8 ms                                                | 96.5 ms: 1.32x slower                                                 |
| fannkuch                   | 240 ms                                                 | 319 ms: 1.33x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 107 ms: 1.35x slower                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.82 ms: 1.36x slower                                                 |
| python_startup             | 10.8 ms                                                | 14.6 ms: 1.36x slower                                                 |
| python_startup_no_site     | 8.57 ms                                                | 12.0 ms: 1.40x slower                                                 |
| pyflate                    | 284 ms                                                 | 399 ms: 1.41x slower                                                  |
| scimark_monte_carlo        | 43.5 ms                                                | 61.4 ms: 1.41x slower                                                 |
| spectral_norm              | 65.7 ms                                                | 94.6 ms: 1.44x slower                                                 |
| logging_silent             | 66.5 ns                                                | 95.9 ns: 1.44x slower                                                 |
| scimark_lu                 | 67.7 ms                                                | 100.0 ms: 1.48x slower                                                |
| flaskblogging              | 2.35 ms                                                | 3.56 ms: 1.51x slower                                                 |
| async_generators           | 192 ms                                                 | 295 ms: 1.54x slower                                                  |
| telco                      | 3.17 ms                                                | 5.05 ms: 1.59x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (3): asyncio_websockets, html5lib, tornado_http
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dulwich_log, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
Ignored benchmarks (8) of results/bm-20240525-3.14.0a0-e418fc3-PYTHON_UOPS/bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.73x