# Results vs. 3.12.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: darwin-arm64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.05x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 180 ms: 1.06x slower                                                   |
| chameleon      | 4.70 ms                                                | 4.76 ms: 1.01x slower                                                  |
| docutils       | 1.50 sec                                               | 1.60 sec: 1.06x slower                                                 |
| tornado_http   | 69.3 ms                                                | 78.6 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 266 ms                                                 | 212 ms: 1.26x faster                                                   |
| async_tree_none_tg         | 258 ms                                                 | 205 ms: 1.25x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 268 ms: 1.21x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 576 ms: 1.16x faster                                                   |
| async_tree_io              | 668 ms                                                 | 579 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 474 ms: 1.12x faster                                                   |
| async_tree_memoization     | 312 ms                                                 | 280 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 473 ms: 1.11x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.17x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| float          | 55.8 ms                                                | 65.0 ms: 1.16x slower                                                  |
| nbody          | 68.8 ms                                                | 84.1 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 154 ms                                                 | 149 ms: 1.04x faster                                                   |
| regex_effbot   | 2.64 ms                                                | 2.57 ms: 1.03x faster                                                  |
| regex_v8       | 16.0 ms                                                | 17.7 ms: 1.11x slower                                                  |
| regex_compile  | 77.9 ms                                                | 95.1 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 188 us: 1.06x faster                                                   |
| unpickle_list        | 3.02 us                                                | 2.93 us: 1.03x faster                                                  |
| json_loads           | 17.2 us                                                | 16.9 us: 1.02x faster                                                  |
| xml_etree_process    | 39.7 ms                                                | 40.0 ms: 1.01x slower                                                  |
| json_dumps           | 6.22 ms                                                | 6.31 ms: 1.01x slower                                                  |
| unpickle             | 9.12 us                                                | 9.26 us: 1.02x slower                                                  |
| pickle_list          | 2.89 us                                                | 2.96 us: 1.03x slower                                                  |
| pickle               | 7.23 us                                                | 7.49 us: 1.04x slower                                                  |
| xml_etree_generate   | 55.8 ms                                                | 58.2 ms: 1.04x slower                                                  |
| xml_etree_iterparse  | 74.0 ms                                                | 77.4 ms: 1.05x slower                                                  |
| tomli_loads          | 1.39 sec                                               | 1.64 sec: 1.18x slower                                                 |
| unpickle_pure_python | 151 us                                                 | 182 us: 1.21x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_parse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 9.37 ms                                                | 10.9 ms: 1.16x slower                                                  |
| python_startup         | 11.4 ms                                                | 13.6 ms: 1.20x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.18x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 22.3 ms                                                | 23.1 ms: 1.03x slower                                                  |
| mako            | 7.71 ms                                                | 9.31 ms: 1.21x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.12x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 266 ms                                                 | 212 ms: 1.26x faster                                                   |
| async_tree_none_tg         | 258 ms                                                 | 205 ms: 1.25x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 268 ms: 1.21x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 576 ms: 1.16x faster                                                   |
| raytrace                   | 212 ms                                                 | 183 ms: 1.16x faster                                                   |
| coroutines                 | 19.2 ms                                                | 16.6 ms: 1.16x faster                                                  |
| async_tree_io              | 668 ms                                                 | 579 ms: 1.15x faster                                                   |
| logging_silent             | 76.4 ns                                                | 66.6 ns: 1.15x faster                                                  |
| generators                 | 31.1 ms                                                | 27.1 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 474 ms: 1.12x faster                                                   |
| async_tree_memoization     | 312 ms                                                 | 280 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 473 ms: 1.11x faster                                                   |
| logging_simple             | 3.69 us                                                | 3.32 us: 1.11x faster                                                  |
| logging_format             | 3.98 us                                                | 3.60 us: 1.11x faster                                                  |
| deepcopy_reduce            | 2.07 us                                                | 1.91 us: 1.09x faster                                                  |
| asyncio_tcp                | 449 ms                                                 | 418 ms: 1.07x faster                                                   |
| pickle_pure_python         | 200 us                                                 | 188 us: 1.06x faster                                                   |
| json                       | 3.09 ms                                                | 2.94 ms: 1.05x faster                                                  |
| deepcopy                   | 235 us                                                 | 225 us: 1.04x faster                                                   |
| regex_dna                  | 154 ms                                                 | 149 ms: 1.04x faster                                                   |
| unpickle_list              | 3.02 us                                                | 2.93 us: 1.03x faster                                                  |
| regex_effbot               | 2.64 ms                                                | 2.57 ms: 1.03x faster                                                  |
| async_generators           | 304 ms                                                 | 296 ms: 1.03x faster                                                   |
| sqlglot_parse              | 848 us                                                 | 832 us: 1.02x faster                                                   |
| json_loads                 | 17.2 us                                                | 16.9 us: 1.02x faster                                                  |
| dulwich_log                | 29.8 ms                                                | 29.3 ms: 1.02x faster                                                  |
| sqlglot_transpile          | 1.02 ms                                                | 1.01 ms: 1.02x faster                                                  |
| asyncio_websockets         | 409 ms                                                 | 408 ms: 1.00x faster                                                   |
| pidigits                   | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| xml_etree_process          | 39.7 ms                                                | 40.0 ms: 1.01x slower                                                  |
| chameleon                  | 4.70 ms                                                | 4.76 ms: 1.01x slower                                                  |
| json_dumps                 | 6.22 ms                                                | 6.31 ms: 1.01x slower                                                  |
| unpickle                   | 9.12 us                                                | 9.26 us: 1.02x slower                                                  |
| sympy_expand               | 241 ms                                                 | 245 ms: 1.02x slower                                                   |
| sqlglot_normalize          | 186 ms                                                 | 189 ms: 1.02x slower                                                   |
| dask                       | 222 ms                                                 | 227 ms: 1.02x slower                                                   |
| bench_thread_pool          | 504 us                                                 | 516 us: 1.02x slower                                                   |
| pickle_list                | 2.89 us                                                | 2.96 us: 1.03x slower                                                  |
| gc_traversal               | 2.40 ms                                                | 2.46 ms: 1.03x slower                                                  |
| sqlite_synth               | 1.57 us                                                | 1.62 us: 1.03x slower                                                  |
| aiohttp                    | 1.08 ms                                                | 1.11 ms: 1.03x slower                                                  |
| django_template            | 22.3 ms                                                | 23.1 ms: 1.03x slower                                                  |
| pickle                     | 7.23 us                                                | 7.49 us: 1.04x slower                                                  |
| xml_etree_generate         | 55.8 ms                                                | 58.2 ms: 1.04x slower                                                  |
| sympy_str                  | 148 ms                                                 | 154 ms: 1.04x slower                                                   |
| sympy_integrate            | 11.4 ms                                                | 11.9 ms: 1.04x slower                                                  |
| xml_etree_iterparse        | 74.0 ms                                                | 77.4 ms: 1.05x slower                                                  |
| gunicorn                   | 1.15 ms                                                | 1.20 ms: 1.05x slower                                                  |
| deltablue                  | 2.71 ms                                                | 2.86 ms: 1.06x slower                                                  |
| 2to3                       | 169 ms                                                 | 180 ms: 1.06x slower                                                   |
| sympy_sum                  | 77.6 ms                                                | 82.3 ms: 1.06x slower                                                  |
| sqlglot_optimize           | 34.0 ms                                                | 36.2 ms: 1.06x slower                                                  |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.32 sec: 1.06x slower                                                 |
| docutils                   | 1.50 sec                                               | 1.60 sec: 1.06x slower                                                 |
| mdp                        | 1.58 sec                                               | 1.68 sec: 1.07x slower                                                 |
| richards_super             | 36.0 ms                                                | 39.0 ms: 1.08x slower                                                  |
| crypto_pyaes               | 51.9 ms                                                | 56.4 ms: 1.09x slower                                                  |
| richards                   | 32.1 ms                                                | 35.5 ms: 1.10x slower                                                  |
| regex_v8                   | 16.0 ms                                                | 17.7 ms: 1.11x slower                                                  |
| meteor_contest             | 71.7 ms                                                | 80.5 ms: 1.12x slower                                                  |
| chaos                      | 42.5 ms                                                | 47.8 ms: 1.12x slower                                                  |
| tornado_http               | 69.3 ms                                                | 78.6 ms: 1.13x slower                                                  |
| coverage                   | 38.9 ms                                                | 44.8 ms: 1.15x slower                                                  |
| nqueens                    | 62.4 ms                                                | 72.1 ms: 1.16x slower                                                  |
| python_startup_no_site     | 9.37 ms                                                | 10.9 ms: 1.16x slower                                                  |
| float                      | 55.8 ms                                                | 65.0 ms: 1.16x slower                                                  |
| go                         | 102 ms                                                 | 119 ms: 1.17x slower                                                   |
| tomli_loads                | 1.39 sec                                               | 1.64 sec: 1.18x slower                                                 |
| typing_runtime_protocols   | 93.0 us                                                | 111 us: 1.19x slower                                                   |
| pprint_safe_repr           | 497 ms                                                 | 593 ms: 1.19x slower                                                   |
| python_startup             | 11.4 ms                                                | 13.6 ms: 1.20x slower                                                  |
| pprint_pformat             | 1.01 sec                                               | 1.21 sec: 1.20x slower                                                 |
| mako                       | 7.71 ms                                                | 9.31 ms: 1.21x slower                                                  |
| unpickle_pure_python       | 151 us                                                 | 182 us: 1.21x slower                                                   |
| scimark_fft                | 195 ms                                                 | 236 ms: 1.21x slower                                                   |
| regex_compile              | 77.9 ms                                                | 95.1 ms: 1.22x slower                                                  |
| nbody                      | 68.8 ms                                                | 84.1 ms: 1.22x slower                                                  |
| comprehensions             | 14.5 us                                                | 17.9 us: 1.23x slower                                                  |
| spectral_norm              | 76.4 ms                                                | 95.2 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.92 ms: 1.25x slower                                                  |
| telco                      | 3.68 ms                                                | 4.64 ms: 1.26x slower                                                  |
| scimark_sor                | 87.4 ms                                                | 111 ms: 1.27x slower                                                   |
| create_gc_cycles           | 701 us                                                 | 905 us: 1.29x slower                                                   |
| pyflate                    | 316 ms                                                 | 411 ms: 1.30x slower                                                   |
| fannkuch                   | 248 ms                                                 | 325 ms: 1.31x slower                                                   |
| mypy2                      | 380 ms                                                 | 502 ms: 1.32x slower                                                   |
| scimark_lu                 | 76.0 ms                                                | 103 ms: 1.35x slower                                                   |
| hexiom                     | 4.54 ms                                                | 6.19 ms: 1.36x slower                                                  |
| scimark_monte_carlo        | 45.0 ms                                                | 63.6 ms: 1.41x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (6): xml_etree_parse, pathlib, deepcopy_memo, bench_mp_pool, pycparser, pickle_dict
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240427-3.13.0a6+-51aefc5-PYTHON_UOPS/bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.05x