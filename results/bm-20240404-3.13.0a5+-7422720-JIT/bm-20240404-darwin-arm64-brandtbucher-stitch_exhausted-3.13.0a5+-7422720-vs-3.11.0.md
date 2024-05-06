# Results vs. 3.11.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: darwin-arm64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.00x slower
- HPT reliability: 97.45%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 173 ms: 1.13x slower                                                     |
| chameleon      | 4.30 ms                                                | 4.46 ms: 1.04x slower                                                    |
| docutils       | 1.43 sec                                               | 1.58 sec: 1.10x slower                                                   |
| html5lib       | 33.0 ms                                                | 31.2 ms: 1.06x faster                                                    |
| tornado_http   | 69.1 ms                                                | 79.8 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                  | 1.07x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none_tg         | 276 ms                                                 | 198 ms: 1.40x faster                                                     |
| async_tree_none            | 282 ms                                                 | 204 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 352 ms                                                 | 261 ms: 1.35x faster                                                     |
| async_tree_io_tg           | 724 ms                                                 | 561 ms: 1.29x faster                                                     |
| async_tree_memoization     | 336 ms                                                 | 262 ms: 1.28x faster                                                     |
| async_tree_io              | 697 ms                                                 | 568 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 467 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 464 ms: 1.12x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 49.5 ms: 1.03x faster                                                    |
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                     |
| nbody          | 61.7 ms                                                | 70.3 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 145 ms: 1.02x faster                                                     |
| regex_effbot   | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                    |
| regex_v8       | 15.1 ms                                                | 17.2 ms: 1.14x slower                                                    |
| regex_compile  | 72.8 ms                                                | 86.1 ms: 1.18x slower                                                    |
| Geometric mean | (ref)                                                  | 1.09x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.37 ms: 1.18x faster                                                    |
| unpickle_pure_python | 149 us                                                 | 140 us: 1.06x faster                                                     |
| pickle_pure_python   | 191 us                                                 | 183 us: 1.05x faster                                                     |
| tomli_loads          | 1.27 sec                                               | 1.29 sec: 1.01x slower                                                   |
| xml_etree_iterparse  | 68.3 ms                                                | 72.2 ms: 1.06x slower                                                    |
| pickle_dict          | 17.1 us                                                | 18.1 us: 1.06x slower                                                    |
| xml_etree_parse      | 100 ms                                                 | 106 ms: 1.06x slower                                                     |
| pickle               | 6.98 us                                                | 7.49 us: 1.07x slower                                                    |
| xml_etree_process    | 33.6 ms                                                | 36.5 ms: 1.09x slower                                                    |
| json_loads           | 15.3 us                                                | 17.1 us: 1.11x slower                                                    |
| pickle_list          | 2.70 us                                                | 3.00 us: 1.11x slower                                                    |
| unpickle             | 8.29 us                                                | 9.27 us: 1.12x slower                                                    |
| unpickle_list        | 2.69 us                                                | 3.04 us: 1.13x slower                                                    |
| xml_etree_generate   | 45.8 ms                                                | 54.3 ms: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 13.5 ms: 1.25x slower                                                    |
| python_startup_no_site | 8.57 ms                                                | 11.7 ms: 1.37x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.31x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 7.93 ms                                                | 6.92 ms: 1.15x faster                                                    |
| genshi_text    | 14.4 ms                                                | 14.7 ms: 1.02x slower                                                    |
| genshi_xml     | 28.5 ms                                                | 33.2 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 70.3 us: 4.28x faster                                                    |
| pylint                     | 253 ms                                                 | 157 ms: 1.61x faster                                                     |
| asyncio_tcp                | 643 ms                                                 | 419 ms: 1.54x faster                                                     |
| async_tree_none_tg         | 276 ms                                                 | 198 ms: 1.40x faster                                                     |
| async_tree_none            | 282 ms                                                 | 204 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 352 ms                                                 | 261 ms: 1.35x faster                                                     |
| async_tree_io_tg           | 724 ms                                                 | 561 ms: 1.29x faster                                                     |
| async_tree_memoization     | 336 ms                                                 | 262 ms: 1.28x faster                                                     |
| raytrace                   | 206 ms                                                 | 165 ms: 1.25x faster                                                     |
| async_tree_io              | 697 ms                                                 | 568 ms: 1.23x faster                                                     |
| chaos                      | 47.4 ms                                                | 38.9 ms: 1.22x faster                                                    |
| comprehensions             | 14.4 us                                                | 12.2 us: 1.19x faster                                                    |
| json_dumps                 | 7.53 ms                                                | 6.37 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 467 ms: 1.18x faster                                                     |
| generators                 | 30.3 ms                                                | 26.1 ms: 1.16x faster                                                    |
| sqlglot_parse              | 890 us                                                 | 772 us: 1.15x faster                                                     |
| mako                       | 7.93 ms                                                | 6.92 ms: 1.15x faster                                                    |
| richards_super             | 37.3 ms                                                | 32.7 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 464 ms: 1.12x faster                                                     |
| deltablue                  | 2.75 ms                                                | 2.48 ms: 1.11x faster                                                    |
| sqlglot_transpile          | 1.05 ms                                                | 948 us: 1.11x faster                                                     |
| logging_simple             | 3.41 us                                                | 3.17 us: 1.07x faster                                                    |
| richards                   | 31.1 ms                                                | 29.1 ms: 1.07x faster                                                    |
| deepcopy_memo              | 25.7 us                                                | 24.2 us: 1.07x faster                                                    |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.31 sec: 1.06x faster                                                   |
| unpickle_pure_python       | 149 us                                                 | 140 us: 1.06x faster                                                     |
| logging_format             | 3.67 us                                                | 3.46 us: 1.06x faster                                                    |
| html5lib                   | 33.0 ms                                                | 31.2 ms: 1.06x faster                                                    |
| pickle_pure_python         | 191 us                                                 | 183 us: 1.05x faster                                                     |
| logging_silent             | 66.5 ns                                                | 63.8 ns: 1.04x faster                                                    |
| sympy_sum                  | 80.2 ms                                                | 77.7 ms: 1.03x faster                                                    |
| float                      | 50.8 ms                                                | 49.5 ms: 1.03x faster                                                    |
| deepcopy                   | 215 us                                                 | 211 us: 1.02x faster                                                     |
| regex_dna                  | 148 ms                                                 | 145 ms: 1.02x faster                                                     |
| crypto_pyaes               | 47.5 ms                                                | 46.9 ms: 1.01x faster                                                    |
| coroutines                 | 17.2 ms                                                | 17.0 ms: 1.01x faster                                                    |
| go                         | 105 ms                                                 | 105 ms: 1.01x faster                                                     |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                     |
| dulwich_log                | 28.6 ms                                                | 29.0 ms: 1.01x slower                                                    |
| tomli_loads                | 1.27 sec                                               | 1.29 sec: 1.01x slower                                                   |
| dask                       | 219 ms                                                 | 222 ms: 1.02x slower                                                     |
| scimark_monte_carlo        | 43.5 ms                                                | 44.3 ms: 1.02x slower                                                    |
| genshi_text                | 14.4 ms                                                | 14.7 ms: 1.02x slower                                                    |
| gc_traversal               | 2.38 ms                                                | 2.45 ms: 1.03x slower                                                    |
| deepcopy_reduce            | 1.79 us                                                | 1.86 us: 1.04x slower                                                    |
| chameleon                  | 4.30 ms                                                | 4.46 ms: 1.04x slower                                                    |
| sympy_integrate            | 11.3 ms                                                | 11.8 ms: 1.04x slower                                                    |
| meteor_contest             | 71.1 ms                                                | 74.3 ms: 1.05x slower                                                    |
| sympy_expand               | 229 ms                                                 | 241 ms: 1.05x slower                                                     |
| regex_effbot               | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                    |
| xml_etree_iterparse        | 68.3 ms                                                | 72.2 ms: 1.06x slower                                                    |
| pprint_pformat             | 979 ms                                                 | 1.04 sec: 1.06x slower                                                   |
| pickle_dict                | 17.1 us                                                | 18.1 us: 1.06x slower                                                    |
| pprint_safe_repr           | 478 ms                                                 | 507 ms: 1.06x slower                                                     |
| xml_etree_parse            | 100 ms                                                 | 106 ms: 1.06x slower                                                     |
| coverage                   | 43.9 ms                                                | 46.5 ms: 1.06x slower                                                    |
| bench_thread_pool          | 465 us                                                 | 495 us: 1.06x slower                                                     |
| mdp                        | 1.48 sec                                               | 1.58 sec: 1.07x slower                                                   |
| json                       | 2.75 ms                                                | 2.94 ms: 1.07x slower                                                    |
| pickle                     | 6.98 us                                                | 7.49 us: 1.07x slower                                                    |
| xml_etree_process          | 33.6 ms                                                | 36.5 ms: 1.09x slower                                                    |
| gunicorn                   | 1.10 ms                                                | 1.19 ms: 1.09x slower                                                    |
| fannkuch                   | 240 ms                                                 | 261 ms: 1.09x slower                                                     |
| pathlib                    | 23.2 ms                                                | 25.3 ms: 1.09x slower                                                    |
| thrift                     | 410 us                                                 | 448 us: 1.09x slower                                                     |
| sqlglot_normalize          | 162 ms                                                 | 178 ms: 1.10x slower                                                     |
| docutils                   | 1.43 sec                                               | 1.58 sec: 1.10x slower                                                   |
| nqueens                    | 55.9 ms                                                | 62.0 ms: 1.11x slower                                                    |
| json_loads                 | 15.3 us                                                | 17.1 us: 1.11x slower                                                    |
| pickle_list                | 2.70 us                                                | 3.00 us: 1.11x slower                                                    |
| aiohttp                    | 1.02 ms                                                | 1.14 ms: 1.11x slower                                                    |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.13 ms: 1.11x slower                                                    |
| unpickle                   | 8.29 us                                                | 9.27 us: 1.12x slower                                                    |
| spectral_norm              | 65.7 ms                                                | 73.5 ms: 1.12x slower                                                    |
| hexiom                     | 4.58 ms                                                | 5.15 ms: 1.12x slower                                                    |
| pyflate                    | 284 ms                                                 | 319 ms: 1.12x slower                                                     |
| 2to3                       | 154 ms                                                 | 173 ms: 1.13x slower                                                     |
| unpickle_list              | 2.69 us                                                | 3.04 us: 1.13x slower                                                    |
| bench_mp_pool              | 41.0 ms                                                | 46.4 ms: 1.13x slower                                                    |
| regex_v8                   | 15.1 ms                                                | 17.2 ms: 1.14x slower                                                    |
| nbody                      | 61.7 ms                                                | 70.3 ms: 1.14x slower                                                    |
| mypy2                      | 372 ms                                                 | 427 ms: 1.15x slower                                                     |
| sqlglot_optimize           | 29.6 ms                                                | 34.2 ms: 1.15x slower                                                    |
| tornado_http               | 69.1 ms                                                | 79.8 ms: 1.16x slower                                                    |
| scimark_fft                | 173 ms                                                 | 201 ms: 1.16x slower                                                     |
| genshi_xml                 | 28.5 ms                                                | 33.2 ms: 1.16x slower                                                    |
| regex_compile              | 72.8 ms                                                | 86.1 ms: 1.18x slower                                                    |
| xml_etree_generate         | 45.8 ms                                                | 54.3 ms: 1.19x slower                                                    |
| scimark_lu                 | 67.7 ms                                                | 81.3 ms: 1.20x slower                                                    |
| python_startup             | 10.8 ms                                                | 13.5 ms: 1.25x slower                                                    |
| create_gc_cycles           | 711 us                                                 | 893 us: 1.26x slower                                                     |
| sqlite_synth               | 1.26 us                                                | 1.58 us: 1.26x slower                                                    |
| scimark_sor                | 79.2 ms                                                | 106 ms: 1.33x slower                                                     |
| python_startup_no_site     | 8.57 ms                                                | 11.7 ms: 1.37x slower                                                    |
| telco                      | 3.17 ms                                                | 4.57 ms: 1.44x slower                                                    |
| async_generators           | 192 ms                                                 | 300 ms: 1.56x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (3): pycparser, sympy_str, asyncio_websockets
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240404-3.13.0a5+-7422720-JIT/bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 97.45% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x