# Results vs. 3.11.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: darwin-arm64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.01x faster
- HPT reliability: 82.34%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 180 ms: 1.17x slower                                                   |
| chameleon      | 4.30 ms                                                | 4.54 ms: 1.06x slower                                                  |
| docutils       | 1.43 sec                                               | 1.45 sec: 1.02x slower                                                 |
| html5lib       | 33.0 ms                                                | 31.9 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 276 ms                                                 | 199 ms: 1.39x faster                                                   |
| async_tree_none            | 282 ms                                                 | 203 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 261 ms: 1.35x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 566 ms: 1.28x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 270 ms: 1.24x faster                                                   |
| async_tree_io              | 697 ms                                                 | 572 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 469 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 466 ms: 1.11x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| float          | 50.8 ms                                                | 52.0 ms: 1.02x slower                                                  |
| nbody          | 61.7 ms                                                | 69.7 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 69.6 ms: 1.05x faster                                                  |
| regex_dna      | 148 ms                                                 | 150 ms: 1.01x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.58 ms: 1.06x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.23 ms: 1.21x faster                                                  |
| unpickle_pure_python | 149 us                                                 | 141 us: 1.06x faster                                                   |
| pickle_pure_python   | 191 us                                                 | 184 us: 1.04x faster                                                   |
| xml_etree_parse      | 100 ms                                                 | 104 ms: 1.04x slower                                                   |
| xml_etree_iterparse  | 68.3 ms                                                | 72.5 ms: 1.06x slower                                                  |
| pickle               | 6.98 us                                                | 7.45 us: 1.07x slower                                                  |
| pickle_dict          | 17.1 us                                                | 18.3 us: 1.07x slower                                                  |
| pickle_list          | 2.70 us                                                | 2.96 us: 1.10x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.95 us: 1.10x slower                                                  |
| json_loads           | 15.3 us                                                | 17.0 us: 1.11x slower                                                  |
| unpickle             | 8.29 us                                                | 9.22 us: 1.11x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 37.6 ms: 1.12x slower                                                  |
| tomli_loads          | 1.27 sec                                               | 1.51 sec: 1.19x slower                                                 |
| xml_etree_generate   | 45.8 ms                                                | 55.1 ms: 1.20x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 8.57 ms                                                | 10.8 ms: 1.25x slower                                                  |
| python_startup         | 10.8 ms                                                | 13.6 ms: 1.26x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 7.93 ms                                                | 7.09 ms: 1.12x faster                                                  |
| genshi_text    | 14.4 ms                                                | 15.0 ms: 1.04x slower                                                  |
| genshi_xml     | 28.5 ms                                                | 31.4 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 94.9 us: 3.17x faster                                                  |
| asyncio_tcp                | 643 ms                                                 | 412 ms: 1.56x faster                                                   |
| pylint                     | 253 ms                                                 | 172 ms: 1.47x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 199 ms: 1.39x faster                                                   |
| async_tree_none            | 282 ms                                                 | 203 ms: 1.39x faster                                                   |
| comprehensions             | 14.4 us                                                | 10.5 us: 1.38x faster                                                  |
| async_tree_memoization_tg  | 352 ms                                                 | 261 ms: 1.35x faster                                                   |
| raytrace                   | 206 ms                                                 | 154 ms: 1.33x faster                                                   |
| chaos                      | 47.4 ms                                                | 36.5 ms: 1.30x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 566 ms: 1.28x faster                                                   |
| deltablue                  | 2.75 ms                                                | 2.21 ms: 1.25x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 270 ms: 1.24x faster                                                   |
| async_tree_io              | 697 ms                                                 | 572 ms: 1.22x faster                                                   |
| json_dumps                 | 7.53 ms                                                | 6.23 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 469 ms: 1.17x faster                                                   |
| sqlglot_parse              | 890 us                                                 | 765 us: 1.16x faster                                                   |
| sqlglot_transpile          | 1.05 ms                                                | 928 us: 1.13x faster                                                   |
| sympy_sum                  | 80.2 ms                                                | 70.9 ms: 1.13x faster                                                  |
| mako                       | 7.93 ms                                                | 7.09 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 466 ms: 1.11x faster                                                   |
| deepcopy_memo              | 25.7 us                                                | 23.6 us: 1.09x faster                                                  |
| sympy_integrate            | 11.3 ms                                                | 10.4 ms: 1.08x faster                                                  |
| hexiom                     | 4.58 ms                                                | 4.25 ms: 1.08x faster                                                  |
| sympy_str                  | 144 ms                                                 | 134 ms: 1.07x faster                                                   |
| logging_simple             | 3.41 us                                                | 3.18 us: 1.07x faster                                                  |
| generators                 | 30.3 ms                                                | 28.3 ms: 1.07x faster                                                  |
| logging_format             | 3.67 us                                                | 3.46 us: 1.06x faster                                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.32 sec: 1.06x faster                                                 |
| unpickle_pure_python       | 149 us                                                 | 141 us: 1.06x faster                                                   |
| richards_super             | 37.3 ms                                                | 35.5 ms: 1.05x faster                                                  |
| regex_compile              | 72.8 ms                                                | 69.6 ms: 1.05x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 184 us: 1.04x faster                                                   |
| go                         | 105 ms                                                 | 102 ms: 1.04x faster                                                   |
| html5lib                   | 33.0 ms                                                | 31.9 ms: 1.03x faster                                                  |
| pycparser                  | 659 ms                                                 | 641 ms: 1.03x faster                                                   |
| logging_silent             | 66.5 ns                                                | 64.9 ns: 1.03x faster                                                  |
| dulwich_log                | 28.6 ms                                                | 27.9 ms: 1.02x faster                                                  |
| coroutines                 | 17.2 ms                                                | 16.9 ms: 1.02x faster                                                  |
| deepcopy                   | 215 us                                                 | 213 us: 1.01x faster                                                   |
| nqueens                    | 55.9 ms                                                | 55.6 ms: 1.01x faster                                                  |
| crypto_pyaes               | 47.5 ms                                                | 47.3 ms: 1.00x faster                                                  |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| meteor_contest             | 71.1 ms                                                | 71.7 ms: 1.01x slower                                                  |
| pprint_pformat             | 979 ms                                                 | 988 ms: 1.01x slower                                                   |
| bench_thread_pool          | 465 us                                                 | 470 us: 1.01x slower                                                   |
| regex_dna                  | 148 ms                                                 | 150 ms: 1.01x slower                                                   |
| pprint_safe_repr           | 478 ms                                                 | 485 ms: 1.01x slower                                                   |
| docutils                   | 1.43 sec                                               | 1.45 sec: 1.02x slower                                                 |
| coverage                   | 43.9 ms                                                | 44.8 ms: 1.02x slower                                                  |
| float                      | 50.8 ms                                                | 52.0 ms: 1.02x slower                                                  |
| scimark_lu                 | 67.7 ms                                                | 69.5 ms: 1.03x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                                  |
| mdp                        | 1.48 sec                                               | 1.54 sec: 1.03x slower                                                 |
| pathlib                    | 23.2 ms                                                | 24.0 ms: 1.04x slower                                                  |
| richards                   | 31.1 ms                                                | 32.2 ms: 1.04x slower                                                  |
| xml_etree_parse            | 100 ms                                                 | 104 ms: 1.04x slower                                                   |
| scimark_monte_carlo        | 43.5 ms                                                | 45.2 ms: 1.04x slower                                                  |
| genshi_text                | 14.4 ms                                                | 15.0 ms: 1.04x slower                                                  |
| aiohttp                    | 1.02 ms                                                | 1.08 ms: 1.05x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.88 us: 1.05x slower                                                  |
| chameleon                  | 4.30 ms                                                | 4.54 ms: 1.06x slower                                                  |
| json                       | 2.75 ms                                                | 2.91 ms: 1.06x slower                                                  |
| regex_effbot               | 2.43 ms                                                | 2.58 ms: 1.06x slower                                                  |
| xml_etree_iterparse        | 68.3 ms                                                | 72.5 ms: 1.06x slower                                                  |
| sqlglot_normalize          | 162 ms                                                 | 173 ms: 1.07x slower                                                   |
| fannkuch                   | 240 ms                                                 | 256 ms: 1.07x slower                                                   |
| pickle                     | 6.98 us                                                | 7.45 us: 1.07x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.3 us: 1.07x slower                                                  |
| bench_mp_pool              | 41.0 ms                                                | 44.0 ms: 1.07x slower                                                  |
| thrift                     | 410 us                                                 | 443 us: 1.08x slower                                                   |
| sqlglot_optimize           | 29.6 ms                                                | 32.2 ms: 1.09x slower                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.07 ms: 1.09x slower                                                  |
| pickle_list                | 2.70 us                                                | 2.96 us: 1.10x slower                                                  |
| spectral_norm              | 65.7 ms                                                | 72.1 ms: 1.10x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 31.4 ms: 1.10x slower                                                  |
| unpickle_list              | 2.69 us                                                | 2.95 us: 1.10x slower                                                  |
| json_loads                 | 15.3 us                                                | 17.0 us: 1.11x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.22 us: 1.11x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 37.6 ms: 1.12x slower                                                  |
| nbody                      | 61.7 ms                                                | 69.7 ms: 1.13x slower                                                  |
| pyflate                    | 284 ms                                                 | 324 ms: 1.14x slower                                                   |
| regex_v8                   | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                  |
| scimark_fft                | 173 ms                                                 | 199 ms: 1.16x slower                                                   |
| 2to3                       | 154 ms                                                 | 180 ms: 1.17x slower                                                   |
| tomli_loads                | 1.27 sec                                               | 1.51 sec: 1.19x slower                                                 |
| xml_etree_generate         | 45.8 ms                                                | 55.1 ms: 1.20x slower                                                  |
| sqlite_synth               | 1.26 us                                                | 1.55 us: 1.24x slower                                                  |
| mypy2                      | 372 ms                                                 | 464 ms: 1.25x slower                                                   |
| scimark_sor                | 79.2 ms                                                | 99.3 ms: 1.25x slower                                                  |
| python_startup_no_site     | 8.57 ms                                                | 10.8 ms: 1.25x slower                                                  |
| python_startup             | 10.8 ms                                                | 13.6 ms: 1.26x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 903 us: 1.27x slower                                                   |
| telco                      | 3.17 ms                                                | 4.47 ms: 1.41x slower                                                  |
| async_generators           | 192 ms                                                 | 287 ms: 1.50x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (6): sympy_expand, asyncio_websockets, django_template, dask, gunicorn, tornado_http
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 82.34% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x