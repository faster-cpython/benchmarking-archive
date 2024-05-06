# Results vs. 3.12.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: darwin-arm64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.04x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 180 ms: 1.06x slower                                                   |
| chameleon      | 4.70 ms                                                | 4.54 ms: 1.04x faster                                                  |
| docutils       | 1.50 sec                                               | 1.45 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 266 ms                                                 | 203 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 258 ms                                                 | 199 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 261 ms: 1.24x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 566 ms: 1.18x faster                                                   |
| async_tree_io              | 668 ms                                                 | 572 ms: 1.17x faster                                                   |
| async_tree_memoization     | 312 ms                                                 | 270 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 469 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 466 ms: 1.13x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.20x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 52.0 ms: 1.07x faster                                                  |
| nbody          | 68.8 ms                                                | 69.7 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 77.9 ms                                                | 69.6 ms: 1.12x faster                                                  |
| regex_dna      | 154 ms                                                 | 150 ms: 1.03x faster                                                   |
| regex_effbot   | 2.64 ms                                                | 2.58 ms: 1.02x faster                                                  |
| regex_v8       | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 184 us: 1.09x faster                                                   |
| unpickle_pure_python | 151 us                                                 | 141 us: 1.07x faster                                                   |
| xml_etree_process    | 39.7 ms                                                | 37.6 ms: 1.05x faster                                                  |
| unpickle_list        | 3.02 us                                                | 2.95 us: 1.02x faster                                                  |
| xml_etree_parse      | 106 ms                                                 | 104 ms: 1.02x faster                                                   |
| xml_etree_iterparse  | 74.0 ms                                                | 72.5 ms: 1.02x faster                                                  |
| xml_etree_generate   | 55.8 ms                                                | 55.1 ms: 1.01x faster                                                  |
| json_loads           | 17.2 us                                                | 17.0 us: 1.01x faster                                                  |
| unpickle             | 9.12 us                                                | 9.22 us: 1.01x slower                                                  |
| pickle_dict          | 18.1 us                                                | 18.3 us: 1.01x slower                                                  |
| pickle_list          | 2.89 us                                                | 2.96 us: 1.02x slower                                                  |
| pickle               | 7.23 us                                                | 7.45 us: 1.03x slower                                                  |
| tomli_loads          | 1.39 sec                                               | 1.51 sec: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 9.37 ms                                                | 10.8 ms: 1.15x slower                                                  |
| python_startup         | 11.4 ms                                                | 13.6 ms: 1.19x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.17x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 22.3 ms                                                | 20.2 ms: 1.10x faster                                                  |
| mako            | 7.71 ms                                                | 7.09 ms: 1.09x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.10x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| comprehensions             | 14.5 us                                                | 10.5 us: 1.39x faster                                                  |
| raytrace                   | 212 ms                                                 | 154 ms: 1.37x faster                                                   |
| async_tree_none            | 266 ms                                                 | 203 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 258 ms                                                 | 199 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 261 ms: 1.24x faster                                                   |
| deltablue                  | 2.71 ms                                                | 2.21 ms: 1.23x faster                                                  |
| async_tree_io_tg           | 669 ms                                                 | 566 ms: 1.18x faster                                                   |
| logging_silent             | 76.4 ns                                                | 64.9 ns: 1.18x faster                                                  |
| deepcopy_memo              | 27.7 us                                                | 23.6 us: 1.17x faster                                                  |
| async_tree_io              | 668 ms                                                 | 572 ms: 1.17x faster                                                   |
| chaos                      | 42.5 ms                                                | 36.5 ms: 1.17x faster                                                  |
| logging_simple             | 3.69 us                                                | 3.18 us: 1.16x faster                                                  |
| async_tree_memoization     | 312 ms                                                 | 270 ms: 1.16x faster                                                   |
| logging_format             | 3.98 us                                                | 3.46 us: 1.15x faster                                                  |
| coroutines                 | 19.2 ms                                                | 16.9 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 469 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 466 ms: 1.13x faster                                                   |
| nqueens                    | 62.4 ms                                                | 55.6 ms: 1.12x faster                                                  |
| regex_compile              | 77.9 ms                                                | 69.6 ms: 1.12x faster                                                  |
| sqlglot_parse              | 848 us                                                 | 765 us: 1.11x faster                                                   |
| django_template            | 22.3 ms                                                | 20.2 ms: 1.10x faster                                                  |
| deepcopy                   | 235 us                                                 | 213 us: 1.10x faster                                                   |
| sympy_str                  | 148 ms                                                 | 134 ms: 1.10x faster                                                   |
| sqlglot_transpile          | 1.02 ms                                                | 928 us: 1.10x faster                                                   |
| deepcopy_reduce            | 2.07 us                                                | 1.88 us: 1.10x faster                                                  |
| generators                 | 31.1 ms                                                | 28.3 ms: 1.10x faster                                                  |
| crypto_pyaes               | 51.9 ms                                                | 47.3 ms: 1.10x faster                                                  |
| sympy_sum                  | 77.6 ms                                                | 70.9 ms: 1.10x faster                                                  |
| scimark_lu                 | 76.0 ms                                                | 69.5 ms: 1.09x faster                                                  |
| asyncio_tcp                | 449 ms                                                 | 412 ms: 1.09x faster                                                   |
| sympy_integrate            | 11.4 ms                                                | 10.4 ms: 1.09x faster                                                  |
| mako                       | 7.71 ms                                                | 7.09 ms: 1.09x faster                                                  |
| pickle_pure_python         | 200 us                                                 | 184 us: 1.09x faster                                                   |
| sqlglot_normalize          | 186 ms                                                 | 173 ms: 1.08x faster                                                   |
| bench_thread_pool          | 504 us                                                 | 470 us: 1.07x faster                                                   |
| float                      | 55.8 ms                                                | 52.0 ms: 1.07x faster                                                  |
| hexiom                     | 4.54 ms                                                | 4.25 ms: 1.07x faster                                                  |
| unpickle_pure_python       | 151 us                                                 | 141 us: 1.07x faster                                                   |
| dulwich_log                | 29.8 ms                                                | 27.9 ms: 1.07x faster                                                  |
| json                       | 3.09 ms                                                | 2.91 ms: 1.06x faster                                                  |
| spectral_norm              | 76.4 ms                                                | 72.1 ms: 1.06x faster                                                  |
| async_generators           | 304 ms                                                 | 287 ms: 1.06x faster                                                   |
| sqlglot_optimize           | 34.0 ms                                                | 32.2 ms: 1.06x faster                                                  |
| pycparser                  | 677 ms                                                 | 641 ms: 1.06x faster                                                   |
| xml_etree_process          | 39.7 ms                                                | 37.6 ms: 1.05x faster                                                  |
| sympy_expand               | 241 ms                                                 | 229 ms: 1.05x faster                                                   |
| chameleon                  | 4.70 ms                                                | 4.54 ms: 1.04x faster                                                  |
| docutils                   | 1.50 sec                                               | 1.45 sec: 1.03x faster                                                 |
| regex_dna                  | 154 ms                                                 | 150 ms: 1.03x faster                                                   |
| mdp                        | 1.58 sec                                               | 1.54 sec: 1.03x faster                                                 |
| pprint_safe_repr           | 497 ms                                                 | 485 ms: 1.02x faster                                                   |
| regex_effbot               | 2.64 ms                                                | 2.58 ms: 1.02x faster                                                  |
| pprint_pformat             | 1.01 sec                                               | 988 ms: 1.02x faster                                                   |
| unpickle_list              | 3.02 us                                                | 2.95 us: 1.02x faster                                                  |
| xml_etree_parse            | 106 ms                                                 | 104 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 74.0 ms                                                | 72.5 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.07 ms: 1.02x faster                                                  |
| bench_mp_pool              | 44.9 ms                                                | 44.0 ms: 1.02x faster                                                  |
| richards_super             | 36.0 ms                                                | 35.5 ms: 1.01x faster                                                  |
| xml_etree_generate         | 55.8 ms                                                | 55.1 ms: 1.01x faster                                                  |
| json_loads                 | 17.2 us                                                | 17.0 us: 1.01x faster                                                  |
| sqlite_synth               | 1.57 us                                                | 1.55 us: 1.01x faster                                                  |
| asyncio_websockets         | 409 ms                                                 | 408 ms: 1.00x faster                                                   |
| meteor_contest             | 71.7 ms                                                | 71.7 ms: 1.00x faster                                                  |
| unpickle                   | 9.12 us                                                | 9.22 us: 1.01x slower                                                  |
| nbody                      | 68.8 ms                                                | 69.7 ms: 1.01x slower                                                  |
| pickle_dict                | 18.1 us                                                | 18.3 us: 1.01x slower                                                  |
| typing_runtime_protocols   | 93.0 us                                                | 94.9 us: 1.02x slower                                                  |
| scimark_fft                | 195 ms                                                 | 199 ms: 1.02x slower                                                   |
| gc_traversal               | 2.40 ms                                                | 2.46 ms: 1.02x slower                                                  |
| pickle_list                | 2.89 us                                                | 2.96 us: 1.02x slower                                                  |
| pyflate                    | 316 ms                                                 | 324 ms: 1.03x slower                                                   |
| fannkuch                   | 248 ms                                                 | 256 ms: 1.03x slower                                                   |
| pickle                     | 7.23 us                                                | 7.45 us: 1.03x slower                                                  |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.32 sec: 1.06x slower                                                 |
| 2to3                       | 169 ms                                                 | 180 ms: 1.06x slower                                                   |
| tomli_loads                | 1.39 sec                                               | 1.51 sec: 1.08x slower                                                 |
| regex_v8                   | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                  |
| scimark_sor                | 87.4 ms                                                | 99.3 ms: 1.14x slower                                                  |
| python_startup_no_site     | 9.37 ms                                                | 10.8 ms: 1.15x slower                                                  |
| coverage                   | 38.9 ms                                                | 44.8 ms: 1.15x slower                                                  |
| python_startup             | 11.4 ms                                                | 13.6 ms: 1.19x slower                                                  |
| telco                      | 3.68 ms                                                | 4.47 ms: 1.21x slower                                                  |
| mypy2                      | 380 ms                                                 | 464 ms: 1.22x slower                                                   |
| create_gc_cycles           | 701 us                                                 | 903 us: 1.29x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (10): gunicorn, pathlib, dask, aiohttp, go, pidigits, json_dumps, richards, scimark_monte_carlo, tornado_http
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.04x