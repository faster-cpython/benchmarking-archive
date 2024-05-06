# Results vs. 3.12.0

- fork: python
- ref: c43f6a4dfaa1c1974141
- machine: darwin-arm64
- commit hash: c43f6a4
- commit date: 2024-04-03
- overall geometric mean: 1.03x faster
- HPT reliability: 99.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 173 ms: 1.02x slower                                                   |
| chameleon      | 4.70 ms                                                | 4.48 ms: 1.05x faster                                                  |
| docutils       | 1.50 sec                                               | 1.56 sec: 1.04x slower                                                 |
| tornado_http   | 69.3 ms                                                | 76.9 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 258 ms                                                 | 197 ms: 1.30x faster                                                   |
| async_tree_none            | 266 ms                                                 | 204 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 261 ms: 1.24x faster                                                   |
| async_tree_memoization     | 312 ms                                                 | 261 ms: 1.20x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 562 ms: 1.19x faster                                                   |
| async_tree_io              | 668 ms                                                 | 566 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 467 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 463 ms: 1.14x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 49.1 ms: 1.14x faster                                                  |
| nbody          | 68.8 ms                                                | 70.5 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 154 ms                                                 | 152 ms: 1.02x faster                                                   |
| regex_effbot   | 2.64 ms                                                | 2.61 ms: 1.01x faster                                                  |
| regex_compile  | 77.9 ms                                                | 80.5 ms: 1.03x slower                                                  |
| regex_v8       | 16.0 ms                                                | 17.2 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 183 us: 1.09x faster                                                   |
| tomli_loads          | 1.39 sec                                               | 1.29 sec: 1.08x faster                                                 |
| xml_etree_process    | 39.7 ms                                                | 37.0 ms: 1.07x faster                                                  |
| unpickle_pure_python | 151 us                                                 | 141 us: 1.07x faster                                                   |
| xml_etree_generate   | 55.8 ms                                                | 54.2 ms: 1.03x faster                                                  |
| xml_etree_iterparse  | 74.0 ms                                                | 72.3 ms: 1.02x faster                                                  |
| json_loads           | 17.2 us                                                | 16.9 us: 1.02x faster                                                  |
| unpickle             | 9.12 us                                                | 9.30 us: 1.02x slower                                                  |
| json_dumps           | 6.22 ms                                                | 6.39 ms: 1.03x slower                                                  |
| pickle_list          | 2.89 us                                                | 2.97 us: 1.03x slower                                                  |
| pickle               | 7.23 us                                                | 7.52 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (3): pickle_dict, unpickle_list, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.4 ms                                                | 13.4 ms: 1.17x slower                                                  |
| python_startup_no_site | 9.37 ms                                                | 11.6 ms: 1.24x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|-----------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako      | 7.71 ms                                                | 6.96 ms: 1.11x faster                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 93.0 us                                                | 69.3 us: 1.34x faster                                                  |
| async_tree_none_tg         | 258 ms                                                 | 197 ms: 1.30x faster                                                   |
| async_tree_none            | 266 ms                                                 | 204 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 261 ms: 1.24x faster                                                   |
| raytrace                   | 212 ms                                                 | 172 ms: 1.23x faster                                                   |
| comprehensions             | 14.5 us                                                | 12.0 us: 1.21x faster                                                  |
| logging_silent             | 76.4 ns                                                | 63.8 ns: 1.20x faster                                                  |
| async_tree_memoization     | 312 ms                                                 | 261 ms: 1.20x faster                                                   |
| deltablue                  | 2.71 ms                                                | 2.27 ms: 1.19x faster                                                  |
| async_tree_io_tg           | 669 ms                                                 | 562 ms: 1.19x faster                                                   |
| generators                 | 31.1 ms                                                | 26.1 ms: 1.19x faster                                                  |
| async_tree_io              | 668 ms                                                 | 566 ms: 1.18x faster                                                   |
| logging_simple             | 3.69 us                                                | 3.13 us: 1.18x faster                                                  |
| logging_format             | 3.98 us                                                | 3.41 us: 1.17x faster                                                  |
| coroutines                 | 19.2 ms                                                | 16.8 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 467 ms: 1.14x faster                                                   |
| float                      | 55.8 ms                                                | 49.1 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 463 ms: 1.14x faster                                                   |
| deepcopy_memo              | 27.7 us                                                | 24.4 us: 1.14x faster                                                  |
| crypto_pyaes               | 51.9 ms                                                | 46.6 ms: 1.11x faster                                                  |
| chaos                      | 42.5 ms                                                | 38.3 ms: 1.11x faster                                                  |
| mako                       | 7.71 ms                                                | 6.96 ms: 1.11x faster                                                  |
| deepcopy_reduce            | 2.07 us                                                | 1.88 us: 1.10x faster                                                  |
| deepcopy                   | 235 us                                                 | 214 us: 1.10x faster                                                   |
| sqlglot_parse              | 848 us                                                 | 774 us: 1.10x faster                                                   |
| pickle_pure_python         | 200 us                                                 | 183 us: 1.09x faster                                                   |
| sqlglot_transpile          | 1.02 ms                                                | 940 us: 1.09x faster                                                   |
| asyncio_tcp                | 449 ms                                                 | 415 ms: 1.08x faster                                                   |
| tomli_loads                | 1.39 sec                                               | 1.29 sec: 1.08x faster                                                 |
| xml_etree_process          | 39.7 ms                                                | 37.0 ms: 1.07x faster                                                  |
| unpickle_pure_python       | 151 us                                                 | 141 us: 1.07x faster                                                   |
| sqlglot_normalize          | 186 ms                                                 | 176 ms: 1.05x faster                                                   |
| chameleon                  | 4.70 ms                                                | 4.48 ms: 1.05x faster                                                  |
| json                       | 3.09 ms                                                | 2.96 ms: 1.04x faster                                                  |
| sympy_str                  | 148 ms                                                 | 142 ms: 1.04x faster                                                   |
| scimark_monte_carlo        | 45.0 ms                                                | 43.2 ms: 1.04x faster                                                  |
| pycparser                  | 677 ms                                                 | 651 ms: 1.04x faster                                                   |
| spectral_norm              | 76.4 ms                                                | 73.7 ms: 1.04x faster                                                  |
| nqueens                    | 62.4 ms                                                | 60.5 ms: 1.03x faster                                                  |
| xml_etree_generate         | 55.8 ms                                                | 54.2 ms: 1.03x faster                                                  |
| bench_thread_pool          | 504 us                                                 | 490 us: 1.03x faster                                                   |
| richards_super             | 36.0 ms                                                | 35.1 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 74.0 ms                                                | 72.3 ms: 1.02x faster                                                  |
| dulwich_log                | 29.8 ms                                                | 29.1 ms: 1.02x faster                                                  |
| json_loads                 | 17.2 us                                                | 16.9 us: 1.02x faster                                                  |
| regex_dna                  | 154 ms                                                 | 152 ms: 1.02x faster                                                   |
| sympy_expand               | 241 ms                                                 | 238 ms: 1.01x faster                                                   |
| richards                   | 32.1 ms                                                | 31.7 ms: 1.01x faster                                                  |
| sympy_sum                  | 77.6 ms                                                | 76.8 ms: 1.01x faster                                                  |
| regex_effbot               | 2.64 ms                                                | 2.61 ms: 1.01x faster                                                  |
| sqlglot_optimize           | 34.0 ms                                                | 33.7 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 497 ms                                                 | 493 ms: 1.01x faster                                                   |
| async_generators           | 304 ms                                                 | 302 ms: 1.01x faster                                                   |
| mdp                        | 1.58 sec                                               | 1.57 sec: 1.00x faster                                                 |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.13 ms: 1.00x faster                                                  |
| sympy_integrate            | 11.4 ms                                                | 11.4 ms: 1.00x slower                                                  |
| sqlite_synth               | 1.57 us                                                | 1.60 us: 1.02x slower                                                  |
| 2to3                       | 169 ms                                                 | 173 ms: 1.02x slower                                                   |
| unpickle                   | 9.12 us                                                | 9.30 us: 1.02x slower                                                  |
| nbody                      | 68.8 ms                                                | 70.5 ms: 1.02x slower                                                  |
| scimark_fft                | 195 ms                                                 | 200 ms: 1.02x slower                                                   |
| meteor_contest             | 71.7 ms                                                | 73.5 ms: 1.02x slower                                                  |
| pyflate                    | 316 ms                                                 | 324 ms: 1.03x slower                                                   |
| gc_traversal               | 2.40 ms                                                | 2.46 ms: 1.03x slower                                                  |
| json_dumps                 | 6.22 ms                                                | 6.39 ms: 1.03x slower                                                  |
| pathlib                    | 24.2 ms                                                | 24.9 ms: 1.03x slower                                                  |
| pickle_list                | 2.89 us                                                | 2.97 us: 1.03x slower                                                  |
| bench_mp_pool              | 44.9 ms                                                | 46.3 ms: 1.03x slower                                                  |
| regex_compile              | 77.9 ms                                                | 80.5 ms: 1.03x slower                                                  |
| docutils                   | 1.50 sec                                               | 1.56 sec: 1.04x slower                                                 |
| pickle                     | 7.23 us                                                | 7.52 us: 1.04x slower                                                  |
| fannkuch                   | 248 ms                                                 | 259 ms: 1.04x slower                                                   |
| go                         | 102 ms                                                 | 106 ms: 1.05x slower                                                   |
| hexiom                     | 4.54 ms                                                | 4.82 ms: 1.06x slower                                                  |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.32 sec: 1.06x slower                                                 |
| scimark_lu                 | 76.0 ms                                                | 81.7 ms: 1.08x slower                                                  |
| regex_v8                   | 16.0 ms                                                | 17.2 ms: 1.08x slower                                                  |
| mypy2                      | 380 ms                                                 | 412 ms: 1.09x slower                                                   |
| tornado_http               | 69.3 ms                                                | 76.9 ms: 1.11x slower                                                  |
| python_startup             | 11.4 ms                                                | 13.4 ms: 1.17x slower                                                  |
| coverage                   | 38.9 ms                                                | 45.9 ms: 1.18x slower                                                  |
| scimark_sor                | 87.4 ms                                                | 106 ms: 1.21x slower                                                   |
| telco                      | 3.68 ms                                                | 4.51 ms: 1.23x slower                                                  |
| python_startup_no_site     | 9.37 ms                                                | 11.6 ms: 1.24x slower                                                  |
| create_gc_cycles           | 701 us                                                 | 896 us: 1.28x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (9): aiohttp, pickle_dict, dask, pprint_pformat, asyncio_websockets, unpickle_list, pidigits, xml_etree_parse, gunicorn
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240403-3.13.0a5+-c43f6a4-JIT/bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x