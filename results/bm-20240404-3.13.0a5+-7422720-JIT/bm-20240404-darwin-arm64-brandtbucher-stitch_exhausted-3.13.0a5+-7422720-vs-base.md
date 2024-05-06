# Results vs. base

- fork: brandtbucher
- ref: stitch_exhausted
- machine: darwin-arm64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.00x slower
- HPT reliability: 99.51%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 172 ms                                                                 | 173 ms: 1.01x slower                                                     |
| chameleon      | 4.49 ms                                                                | 4.46 ms: 1.01x faster                                                    |
| docutils       | 1.56 sec                                                               | 1.58 sec: 1.01x slower                                                   |
| html5lib       | 34.6 ms                                                                | 31.2 ms: 1.11x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io              | 576 ms                                                                 | 568 ms: 1.02x faster                                                     |
| async_tree_eager_tg        | 43.8 ms                                                                | 43.3 ms: 1.01x faster                                                    |
| async_tree_eager           | 64.8 ms                                                                | 66.3 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed_tg | 455 ms                                                                 | 467 ms: 1.03x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (12): async_tree_eager_memoization_tg, async_tree_io_tg, async_tree_eager_io, async_tree_memoization_tg, async_tree_eager_io_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_memoization, async_tree_memoization, async_tree_none, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 70.7 ms                                                                | 70.3 ms: 1.01x faster                                                    |
| pidigits       | 283 ms                                                                 | 282 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.89 ms                                                                | 2.56 ms: 1.13x faster                                                    |
| regex_dna      | 157 ms                                                                 | 145 ms: 1.08x faster                                                     |
| regex_v8       | 17.4 ms                                                                | 17.2 ms: 1.01x faster                                                    |
| regex_compile  | 85.6 ms                                                                | 86.1 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle             | 9.67 us                                                                | 9.27 us: 1.04x faster                                                    |
| xml_etree_process    | 37.3 ms                                                                | 36.5 ms: 1.02x faster                                                    |
| xml_etree_iterparse  | 72.9 ms                                                                | 72.2 ms: 1.01x faster                                                    |
| xml_etree_parse      | 107 ms                                                                 | 106 ms: 1.01x faster                                                     |
| xml_etree_generate   | 54.7 ms                                                                | 54.3 ms: 1.01x faster                                                    |
| unpickle_pure_python | 141 us                                                                 | 140 us: 1.01x faster                                                     |
| pickle_dict          | 18.1 us                                                                | 18.1 us: 1.00x slower                                                    |
| pickle               | 7.45 us                                                                | 7.49 us: 1.00x slower                                                    |
| json_dumps           | 6.33 ms                                                                | 6.37 ms: 1.01x slower                                                    |
| tomli_loads          | 1.28 sec                                                               | 1.29 sec: 1.01x slower                                                   |
| pickle_list          | 2.97 us                                                                | 3.00 us: 1.01x slower                                                    |
| json_loads           | 16.9 us                                                                | 17.1 us: 1.01x slower                                                    |
| pickle_pure_python   | 180 us                                                                 | 183 us: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 11.6 ms                                                                | 11.7 ms: 1.01x slower                                                    |
| python_startup         | 13.3 ms                                                                | 13.5 ms: 1.01x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text    | 14.8 ms                                                                | 14.7 ms: 1.01x faster                                                    |
| genshi_xml     | 31.5 ms                                                                | 33.2 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot               | 2.89 ms                                                                | 2.56 ms: 1.13x faster                                                    |
| html5lib                   | 34.6 ms                                                                | 31.2 ms: 1.11x faster                                                    |
| regex_dna                  | 157 ms                                                                 | 145 ms: 1.08x faster                                                     |
| unpickle                   | 9.67 us                                                                | 9.27 us: 1.04x faster                                                    |
| logging_silent             | 65.4 ns                                                                | 63.8 ns: 1.03x faster                                                    |
| xml_etree_process          | 37.3 ms                                                                | 36.5 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult    | 3.20 ms                                                                | 3.13 ms: 1.02x faster                                                    |
| scimark_lu                 | 82.7 ms                                                                | 81.3 ms: 1.02x faster                                                    |
| telco                      | 4.65 ms                                                                | 4.57 ms: 1.02x faster                                                    |
| async_tree_io              | 576 ms                                                                 | 568 ms: 1.02x faster                                                     |
| go                         | 106 ms                                                                 | 105 ms: 1.02x faster                                                     |
| regex_v8                   | 17.4 ms                                                                | 17.2 ms: 1.01x faster                                                    |
| async_tree_eager_tg        | 43.8 ms                                                                | 43.3 ms: 1.01x faster                                                    |
| xml_etree_iterparse        | 72.9 ms                                                                | 72.2 ms: 1.01x faster                                                    |
| xml_etree_parse            | 107 ms                                                                 | 106 ms: 1.01x faster                                                     |
| create_gc_cycles           | 901 us                                                                 | 893 us: 1.01x faster                                                     |
| genshi_text                | 14.8 ms                                                                | 14.7 ms: 1.01x faster                                                    |
| generators                 | 26.3 ms                                                                | 26.1 ms: 1.01x faster                                                    |
| coverage                   | 46.9 ms                                                                | 46.5 ms: 1.01x faster                                                    |
| chameleon                  | 4.49 ms                                                                | 4.46 ms: 1.01x faster                                                    |
| xml_etree_generate         | 54.7 ms                                                                | 54.3 ms: 1.01x faster                                                    |
| nbody                      | 70.7 ms                                                                | 70.3 ms: 1.01x faster                                                    |
| unpickle_pure_python       | 141 us                                                                 | 140 us: 1.01x faster                                                     |
| richards                   | 29.2 ms                                                                | 29.1 ms: 1.01x faster                                                    |
| sqlite_synth               | 1.59 us                                                                | 1.58 us: 1.00x faster                                                    |
| richards_super             | 32.9 ms                                                                | 32.7 ms: 1.00x faster                                                    |
| deepcopy                   | 211 us                                                                 | 211 us: 1.00x faster                                                     |
| dulwich_log                | 29.0 ms                                                                | 29.0 ms: 1.00x faster                                                    |
| spectral_norm              | 73.7 ms                                                                | 73.5 ms: 1.00x faster                                                    |
| scimark_sor                | 106 ms                                                                 | 106 ms: 1.00x faster                                                     |
| gc_traversal               | 2.46 ms                                                                | 2.45 ms: 1.00x faster                                                    |
| pidigits                   | 283 ms                                                                 | 282 ms: 1.00x faster                                                     |
| asyncio_websockets         | 409 ms                                                                 | 408 ms: 1.00x faster                                                     |
| deepcopy_memo              | 24.1 us                                                                | 24.2 us: 1.00x slower                                                    |
| mdp                        | 1.58 sec                                                               | 1.58 sec: 1.00x slower                                                   |
| pickle_dict                | 18.1 us                                                                | 18.1 us: 1.00x slower                                                    |
| pickle                     | 7.45 us                                                                | 7.49 us: 1.00x slower                                                    |
| async_generators           | 299 ms                                                                 | 300 ms: 1.01x slower                                                     |
| json_dumps                 | 6.33 ms                                                                | 6.37 ms: 1.01x slower                                                    |
| regex_compile              | 85.6 ms                                                                | 86.1 ms: 1.01x slower                                                    |
| crypto_pyaes               | 46.5 ms                                                                | 46.9 ms: 1.01x slower                                                    |
| tomli_loads                | 1.28 sec                                                               | 1.29 sec: 1.01x slower                                                   |
| python_startup_no_site     | 11.6 ms                                                                | 11.7 ms: 1.01x slower                                                    |
| pickle_list                | 2.97 us                                                                | 3.00 us: 1.01x slower                                                    |
| chaos                      | 38.6 ms                                                                | 38.9 ms: 1.01x slower                                                    |
| sqlglot_normalize          | 176 ms                                                                 | 178 ms: 1.01x slower                                                     |
| pyflate                    | 316 ms                                                                 | 319 ms: 1.01x slower                                                     |
| sqlglot_parse              | 765 us                                                                 | 772 us: 1.01x slower                                                     |
| python_startup             | 13.3 ms                                                                | 13.5 ms: 1.01x slower                                                    |
| sqlglot_transpile          | 939 us                                                                 | 948 us: 1.01x slower                                                     |
| json_loads                 | 16.9 us                                                                | 17.1 us: 1.01x slower                                                    |
| logging_format             | 3.43 us                                                                | 3.46 us: 1.01x slower                                                    |
| 2to3                       | 172 ms                                                                 | 173 ms: 1.01x slower                                                     |
| docutils                   | 1.56 sec                                                               | 1.58 sec: 1.01x slower                                                   |
| scimark_monte_carlo        | 43.8 ms                                                                | 44.3 ms: 1.01x slower                                                    |
| sympy_str                  | 142 ms                                                                 | 144 ms: 1.01x slower                                                     |
| comprehensions             | 12.0 us                                                                | 12.2 us: 1.01x slower                                                    |
| raytrace                   | 163 ms                                                                 | 165 ms: 1.01x slower                                                     |
| meteor_contest             | 73.4 ms                                                                | 74.3 ms: 1.01x slower                                                    |
| sqlglot_optimize           | 33.7 ms                                                                | 34.2 ms: 1.01x slower                                                    |
| sympy_sum                  | 76.6 ms                                                                | 77.7 ms: 1.01x slower                                                    |
| sympy_expand               | 237 ms                                                                 | 241 ms: 1.02x slower                                                     |
| pickle_pure_python         | 180 us                                                                 | 183 us: 1.02x slower                                                     |
| typing_runtime_protocols   | 69.1 us                                                                | 70.3 us: 1.02x slower                                                    |
| logging_simple             | 3.12 us                                                                | 3.17 us: 1.02x slower                                                    |
| bench_thread_pool          | 486 us                                                                 | 495 us: 1.02x slower                                                     |
| pylint                     | 154 ms                                                                 | 157 ms: 1.02x slower                                                     |
| async_tree_eager           | 64.8 ms                                                                | 66.3 ms: 1.02x slower                                                    |
| nqueens                    | 60.4 ms                                                                | 62.0 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed_tg | 455 ms                                                                 | 467 ms: 1.03x slower                                                     |
| pprint_safe_repr           | 492 ms                                                                 | 507 ms: 1.03x slower                                                     |
| sympy_integrate            | 11.4 ms                                                                | 11.8 ms: 1.03x slower                                                    |
| pprint_pformat             | 1.00 sec                                                               | 1.04 sec: 1.03x slower                                                   |
| mypy2                      | 409 ms                                                                 | 427 ms: 1.04x slower                                                     |
| genshi_xml                 | 31.5 ms                                                                | 33.2 ms: 1.05x slower                                                    |
| aiohttp                    | 1.07 ms                                                                | 1.14 ms: 1.06x slower                                                    |
| hexiom                     | 4.81 ms                                                                | 5.15 ms: 1.07x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (30): thrift, unpickle_list, json, async_tree_eager_memoization_tg, mako, async_tree_io_tg, async_tree_eager_io, async_tree_memoization_tg, async_tree_eager_io_tg, async_tree_eager_cpu_io_mixed_tg, fannkuch, scimark_fft, deltablue, async_tree_eager_memoization, gunicorn, deepcopy_reduce, pycparser, asyncio_tcp_ssl, async_tree_memoization, async_tree_none, async_tree_none_tg, float, async_tree_cpu_io_mixed, async_tree_eager_cpu_io_mixed, coroutines, bench_mp_pool, dask, pathlib, tornado_http, asyncio_tcp

# HPT report

- Reliability score: 99.51% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x