# Results vs. 3.12.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: darwin-arm64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.03x slower
- HPT reliability: 97.58%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 172 ms: 1.02x slower                                                   |
| docutils       | 1.50 sec                                               | 1.57 sec: 1.04x slower                                                 |
| tornado_http   | 69.3 ms                                                | 78.8 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 258 ms                                                 | 204 ms: 1.26x faster                                                   |
| async_tree_none            | 266 ms                                                 | 212 ms: 1.25x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 265 ms: 1.22x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 568 ms: 1.18x faster                                                   |
| async_tree_io              | 668 ms                                                 | 576 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 470 ms: 1.13x faster                                                   |
| async_tree_memoization     | 312 ms                                                 | 280 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 472 ms: 1.11x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.18x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| float          | 55.8 ms                                                | 64.7 ms: 1.16x slower                                                  |
| nbody          | 68.8 ms                                                | 83.4 ms: 1.21x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 154 ms                                                 | 149 ms: 1.04x faster                                                   |
| regex_effbot   | 2.64 ms                                                | 2.63 ms: 1.00x faster                                                  |
| regex_v8       | 16.0 ms                                                | 17.6 ms: 1.10x slower                                                  |
| regex_compile  | 77.9 ms                                                | 92.8 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 184 us: 1.09x faster                                                   |
| xml_etree_parse      | 106 ms                                                 | 99.0 ms: 1.07x faster                                                  |
| unpickle_list        | 3.02 us                                                | 2.91 us: 1.04x faster                                                  |
| xml_etree_process    | 39.7 ms                                                | 39.1 ms: 1.01x faster                                                  |
| json_loads           | 17.2 us                                                | 17.0 us: 1.01x faster                                                  |
| xml_etree_iterparse  | 74.0 ms                                                | 73.0 ms: 1.01x faster                                                  |
| pickle_dict          | 18.1 us                                                | 18.1 us: 1.00x slower                                                  |
| unpickle             | 9.12 us                                                | 9.21 us: 1.01x slower                                                  |
| xml_etree_generate   | 55.8 ms                                                | 56.8 ms: 1.02x slower                                                  |
| json_dumps           | 6.22 ms                                                | 6.39 ms: 1.03x slower                                                  |
| pickle               | 7.23 us                                                | 7.47 us: 1.03x slower                                                  |
| pickle_list          | 2.89 us                                                | 3.02 us: 1.04x slower                                                  |
| tomli_loads          | 1.39 sec                                               | 1.66 sec: 1.19x slower                                                 |
| unpickle_pure_python | 151 us                                                 | 181 us: 1.20x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 9.37 ms                                                | 9.19 ms: 1.02x faster                                                  |
| python_startup         | 11.4 ms                                                | 12.0 ms: 1.05x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 7.71 ms                                                | 9.33 ms: 1.21x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 93.0 us                                                | 71.2 us: 1.31x faster                                                  |
| async_tree_none_tg         | 258 ms                                                 | 204 ms: 1.26x faster                                                   |
| async_tree_none            | 266 ms                                                 | 212 ms: 1.25x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 265 ms: 1.22x faster                                                   |
| generators                 | 31.1 ms                                                | 26.0 ms: 1.20x faster                                                  |
| async_tree_io_tg           | 669 ms                                                 | 568 ms: 1.18x faster                                                   |
| raytrace                   | 212 ms                                                 | 181 ms: 1.17x faster                                                   |
| logging_silent             | 76.4 ns                                                | 65.6 ns: 1.17x faster                                                  |
| async_tree_io              | 668 ms                                                 | 576 ms: 1.16x faster                                                   |
| logging_format             | 3.98 us                                                | 3.47 us: 1.15x faster                                                  |
| coroutines                 | 19.2 ms                                                | 16.8 ms: 1.15x faster                                                  |
| logging_simple             | 3.69 us                                                | 3.21 us: 1.15x faster                                                  |
| asyncio_tcp                | 449 ms                                                 | 393 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 470 ms: 1.13x faster                                                   |
| async_tree_memoization     | 312 ms                                                 | 280 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 472 ms: 1.11x faster                                                   |
| deepcopy_reduce            | 2.07 us                                                | 1.90 us: 1.09x faster                                                  |
| pickle_pure_python         | 200 us                                                 | 184 us: 1.09x faster                                                   |
| xml_etree_parse            | 106 ms                                                 | 99.0 ms: 1.07x faster                                                  |
| deepcopy                   | 235 us                                                 | 219 us: 1.07x faster                                                   |
| json                       | 3.09 ms                                                | 2.93 ms: 1.05x faster                                                  |
| unpickle_list              | 3.02 us                                                | 2.91 us: 1.04x faster                                                  |
| regex_dna                  | 154 ms                                                 | 149 ms: 1.04x faster                                                   |
| async_generators           | 304 ms                                                 | 294 ms: 1.04x faster                                                   |
| dulwich_log                | 29.8 ms                                                | 28.9 ms: 1.03x faster                                                  |
| bench_mp_pool              | 44.9 ms                                                | 43.6 ms: 1.03x faster                                                  |
| sqlglot_normalize          | 186 ms                                                 | 181 ms: 1.02x faster                                                   |
| sqlglot_transpile          | 1.02 ms                                                | 1.00 ms: 1.02x faster                                                  |
| python_startup_no_site     | 9.37 ms                                                | 9.19 ms: 1.02x faster                                                  |
| sqlglot_parse              | 848 us                                                 | 833 us: 1.02x faster                                                   |
| xml_etree_process          | 39.7 ms                                                | 39.1 ms: 1.01x faster                                                  |
| json_loads                 | 17.2 us                                                | 17.0 us: 1.01x faster                                                  |
| xml_etree_iterparse        | 74.0 ms                                                | 73.0 ms: 1.01x faster                                                  |
| deepcopy_memo              | 27.7 us                                                | 27.3 us: 1.01x faster                                                  |
| pycparser                  | 677 ms                                                 | 672 ms: 1.01x faster                                                   |
| regex_effbot               | 2.64 ms                                                | 2.63 ms: 1.00x faster                                                  |
| pickle_dict                | 18.1 us                                                | 18.1 us: 1.00x slower                                                  |
| pidigits                   | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| unpickle                   | 9.12 us                                                | 9.21 us: 1.01x slower                                                  |
| sympy_expand               | 241 ms                                                 | 244 ms: 1.01x slower                                                   |
| 2to3                       | 169 ms                                                 | 172 ms: 1.02x slower                                                   |
| xml_etree_generate         | 55.8 ms                                                | 56.8 ms: 1.02x slower                                                  |
| mdp                        | 1.58 sec                                               | 1.61 sec: 1.02x slower                                                 |
| gc_traversal               | 2.40 ms                                                | 2.45 ms: 1.02x slower                                                  |
| sympy_str                  | 148 ms                                                 | 151 ms: 1.03x slower                                                   |
| json_dumps                 | 6.22 ms                                                | 6.39 ms: 1.03x slower                                                  |
| sqlglot_optimize           | 34.0 ms                                                | 35.2 ms: 1.03x slower                                                  |
| pickle                     | 7.23 us                                                | 7.47 us: 1.03x slower                                                  |
| sympy_integrate            | 11.4 ms                                                | 11.8 ms: 1.03x slower                                                  |
| sqlite_synth               | 1.57 us                                                | 1.63 us: 1.04x slower                                                  |
| deltablue                  | 2.71 ms                                                | 2.81 ms: 1.04x slower                                                  |
| sympy_sum                  | 77.6 ms                                                | 81.0 ms: 1.04x slower                                                  |
| docutils                   | 1.50 sec                                               | 1.57 sec: 1.04x slower                                                 |
| pickle_list                | 2.89 us                                                | 3.02 us: 1.04x slower                                                  |
| python_startup             | 11.4 ms                                                | 12.0 ms: 1.05x slower                                                  |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.32 sec: 1.06x slower                                                 |
| aiohttp                    | 1.08 ms                                                | 1.15 ms: 1.07x slower                                                  |
| mypy2                      | 380 ms                                                 | 408 ms: 1.07x slower                                                   |
| richards_super             | 36.0 ms                                                | 39.0 ms: 1.08x slower                                                  |
| crypto_pyaes               | 51.9 ms                                                | 56.6 ms: 1.09x slower                                                  |
| meteor_contest             | 71.7 ms                                                | 78.9 ms: 1.10x slower                                                  |
| regex_v8                   | 16.0 ms                                                | 17.6 ms: 1.10x slower                                                  |
| richards                   | 32.1 ms                                                | 35.4 ms: 1.10x slower                                                  |
| nqueens                    | 62.4 ms                                                | 69.9 ms: 1.12x slower                                                  |
| comprehensions             | 14.5 us                                                | 16.5 us: 1.14x slower                                                  |
| tornado_http               | 69.3 ms                                                | 78.8 ms: 1.14x slower                                                  |
| chaos                      | 42.5 ms                                                | 48.4 ms: 1.14x slower                                                  |
| float                      | 55.8 ms                                                | 64.7 ms: 1.16x slower                                                  |
| go                         | 102 ms                                                 | 119 ms: 1.17x slower                                                   |
| pprint_safe_repr           | 497 ms                                                 | 587 ms: 1.18x slower                                                   |
| pprint_pformat             | 1.01 sec                                               | 1.20 sec: 1.19x slower                                                 |
| coverage                   | 38.9 ms                                                | 46.2 ms: 1.19x slower                                                  |
| tomli_loads                | 1.39 sec                                               | 1.66 sec: 1.19x slower                                                 |
| regex_compile              | 77.9 ms                                                | 92.8 ms: 1.19x slower                                                  |
| unpickle_pure_python       | 151 us                                                 | 181 us: 1.20x slower                                                   |
| mako                       | 7.71 ms                                                | 9.33 ms: 1.21x slower                                                  |
| nbody                      | 68.8 ms                                                | 83.4 ms: 1.21x slower                                                  |
| create_gc_cycles           | 701 us                                                 | 877 us: 1.25x slower                                                   |
| scimark_fft                | 195 ms                                                 | 246 ms: 1.26x slower                                                   |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 4.00 ms: 1.28x slower                                                  |
| telco                      | 3.68 ms                                                | 4.72 ms: 1.28x slower                                                  |
| scimark_sor                | 87.4 ms                                                | 112 ms: 1.28x slower                                                   |
| hexiom                     | 4.54 ms                                                | 5.96 ms: 1.31x slower                                                  |
| spectral_norm              | 76.4 ms                                                | 100 ms: 1.31x slower                                                   |
| pyflate                    | 316 ms                                                 | 418 ms: 1.33x slower                                                   |
| scimark_lu                 | 76.0 ms                                                | 101 ms: 1.33x slower                                                   |
| fannkuch                   | 248 ms                                                 | 341 ms: 1.37x slower                                                   |
| scimark_monte_carlo        | 45.0 ms                                                | 64.3 ms: 1.43x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (7): pathlib, chameleon, bench_thread_pool, asyncio_websockets, django_template, dask, gunicorn
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 97.58% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.05x