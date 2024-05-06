# Results vs. 3.12.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: darwin-arm64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.06x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 178 ms: 1.05x slower                                                   |
| chameleon      | 4.70 ms                                                | 4.83 ms: 1.03x slower                                                  |
| docutils       | 1.50 sec                                               | 1.62 sec: 1.08x slower                                                 |
| tornado_http   | 69.3 ms                                                | 80.3 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 258 ms                                                 | 209 ms: 1.23x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 270 ms: 1.20x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 570 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 464 ms: 1.15x faster                                                   |
| async_tree_io              | 668 ms                                                 | 584 ms: 1.14x faster                                                   |
| async_tree_memoization     | 312 ms                                                 | 276 ms: 1.13x faster                                                   |
| async_tree_none            | 266 ms                                                 | 236 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 471 ms: 1.12x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.16x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                 | 283 ms: 1.01x slower                                                   |
| float          | 55.8 ms                                                | 69.4 ms: 1.24x slower                                                  |
| nbody          | 68.8 ms                                                | 86.7 ms: 1.26x slower                                                  |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.64 ms                                                | 2.56 ms: 1.03x faster                                                  |
| regex_dna      | 154 ms                                                 | 152 ms: 1.01x faster                                                   |
| regex_v8       | 16.0 ms                                                | 17.2 ms: 1.08x slower                                                  |
| regex_compile  | 77.9 ms                                                | 92.7 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 189 us: 1.06x faster                                                   |
| json_loads           | 17.2 us                                                | 17.0 us: 1.01x faster                                                  |
| xml_etree_process    | 39.7 ms                                                | 39.2 ms: 1.01x faster                                                  |
| pickle_dict          | 18.1 us                                                | 18.1 us: 1.00x slower                                                  |
| json_dumps           | 6.22 ms                                                | 6.28 ms: 1.01x slower                                                  |
| unpickle_list        | 3.02 us                                                | 3.05 us: 1.01x slower                                                  |
| pickle               | 7.23 us                                                | 7.52 us: 1.04x slower                                                  |
| pickle_list          | 2.89 us                                                | 3.01 us: 1.04x slower                                                  |
| xml_etree_generate   | 55.8 ms                                                | 58.9 ms: 1.05x slower                                                  |
| xml_etree_iterparse  | 74.0 ms                                                | 79.5 ms: 1.07x slower                                                  |
| tomli_loads          | 1.39 sec                                               | 1.69 sec: 1.21x slower                                                 |
| unpickle_pure_python | 151 us                                                 | 188 us: 1.25x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (2): unpickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.4 ms                                                | 12.0 ms: 1.05x slower                                                  |
| python_startup_no_site | 9.37 ms                                                | 10.3 ms: 1.10x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 22.3 ms                                                | 22.6 ms: 1.01x slower                                                  |
| mako            | 7.71 ms                                                | 9.32 ms: 1.21x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.11x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 93.0 us                                                | 72.6 us: 1.28x faster                                                  |
| async_tree_none_tg         | 258 ms                                                 | 209 ms: 1.23x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 270 ms: 1.20x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 570 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 464 ms: 1.15x faster                                                   |
| async_tree_io              | 668 ms                                                 | 584 ms: 1.14x faster                                                   |
| coroutines                 | 19.2 ms                                                | 17.0 ms: 1.13x faster                                                  |
| async_tree_memoization     | 312 ms                                                 | 276 ms: 1.13x faster                                                   |
| logging_silent             | 76.4 ns                                                | 67.9 ns: 1.13x faster                                                  |
| async_tree_none            | 266 ms                                                 | 236 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 471 ms: 1.12x faster                                                   |
| generators                 | 31.1 ms                                                | 28.0 ms: 1.11x faster                                                  |
| logging_simple             | 3.69 us                                                | 3.39 us: 1.09x faster                                                  |
| logging_format             | 3.98 us                                                | 3.68 us: 1.08x faster                                                  |
| deepcopy_reduce            | 2.07 us                                                | 1.92 us: 1.08x faster                                                  |
| pickle_pure_python         | 200 us                                                 | 189 us: 1.06x faster                                                   |
| deepcopy                   | 235 us                                                 | 222 us: 1.06x faster                                                   |
| json                       | 3.09 ms                                                | 2.98 ms: 1.04x faster                                                  |
| regex_effbot               | 2.64 ms                                                | 2.56 ms: 1.03x faster                                                  |
| deltablue                  | 2.71 ms                                                | 2.63 ms: 1.03x faster                                                  |
| bench_mp_pool              | 44.9 ms                                                | 43.8 ms: 1.02x faster                                                  |
| regex_dna                  | 154 ms                                                 | 152 ms: 1.01x faster                                                   |
| json_loads                 | 17.2 us                                                | 17.0 us: 1.01x faster                                                  |
| xml_etree_process          | 39.7 ms                                                | 39.2 ms: 1.01x faster                                                  |
| sqlglot_transpile          | 1.02 ms                                                | 1.01 ms: 1.01x faster                                                  |
| sqlglot_parse              | 848 us                                                 | 843 us: 1.01x faster                                                   |
| asyncio_websockets         | 409 ms                                                 | 408 ms: 1.00x faster                                                   |
| pickle_dict                | 18.1 us                                                | 18.1 us: 1.00x slower                                                  |
| pidigits                   | 282 ms                                                 | 283 ms: 1.01x slower                                                   |
| json_dumps                 | 6.22 ms                                                | 6.28 ms: 1.01x slower                                                  |
| unpickle_list              | 3.02 us                                                | 3.05 us: 1.01x slower                                                  |
| deepcopy_memo              | 27.7 us                                                | 28.0 us: 1.01x slower                                                  |
| raytrace                   | 212 ms                                                 | 215 ms: 1.01x slower                                                   |
| django_template            | 22.3 ms                                                | 22.6 ms: 1.01x slower                                                  |
| dulwich_log                | 29.8 ms                                                | 30.4 ms: 1.02x slower                                                  |
| gc_traversal               | 2.40 ms                                                | 2.45 ms: 1.02x slower                                                  |
| sympy_expand               | 241 ms                                                 | 247 ms: 1.02x slower                                                   |
| bench_thread_pool          | 504 us                                                 | 517 us: 1.03x slower                                                   |
| chameleon                  | 4.70 ms                                                | 4.83 ms: 1.03x slower                                                  |
| mdp                        | 1.58 sec                                               | 1.64 sec: 1.04x slower                                                 |
| sympy_str                  | 148 ms                                                 | 153 ms: 1.04x slower                                                   |
| pathlib                    | 24.2 ms                                                | 25.1 ms: 1.04x slower                                                  |
| pickle                     | 7.23 us                                                | 7.52 us: 1.04x slower                                                  |
| pycparser                  | 677 ms                                                 | 705 ms: 1.04x slower                                                   |
| pickle_list                | 2.89 us                                                | 3.01 us: 1.04x slower                                                  |
| sqlglot_optimize           | 34.0 ms                                                | 35.7 ms: 1.05x slower                                                  |
| python_startup             | 11.4 ms                                                | 12.0 ms: 1.05x slower                                                  |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.31 sec: 1.05x slower                                                 |
| 2to3                       | 169 ms                                                 | 178 ms: 1.05x slower                                                   |
| sqlite_synth               | 1.57 us                                                | 1.65 us: 1.05x slower                                                  |
| xml_etree_generate         | 55.8 ms                                                | 58.9 ms: 1.05x slower                                                  |
| sympy_integrate            | 11.4 ms                                                | 12.0 ms: 1.06x slower                                                  |
| sympy_sum                  | 77.6 ms                                                | 82.3 ms: 1.06x slower                                                  |
| xml_etree_iterparse        | 74.0 ms                                                | 79.5 ms: 1.07x slower                                                  |
| docutils                   | 1.50 sec                                               | 1.62 sec: 1.08x slower                                                 |
| regex_v8                   | 16.0 ms                                                | 17.2 ms: 1.08x slower                                                  |
| crypto_pyaes               | 51.9 ms                                                | 56.7 ms: 1.09x slower                                                  |
| python_startup_no_site     | 9.37 ms                                                | 10.3 ms: 1.10x slower                                                  |
| mypy2                      | 380 ms                                                 | 417 ms: 1.10x slower                                                   |
| chaos                      | 42.5 ms                                                | 48.0 ms: 1.13x slower                                                  |
| meteor_contest             | 71.7 ms                                                | 81.1 ms: 1.13x slower                                                  |
| unpack_sequence            | 31.5 ns                                                | 35.8 ns: 1.14x slower                                                  |
| richards_super             | 36.0 ms                                                | 41.8 ms: 1.16x slower                                                  |
| tornado_http               | 69.3 ms                                                | 80.3 ms: 1.16x slower                                                  |
| go                         | 102 ms                                                 | 118 ms: 1.16x slower                                                   |
| pprint_safe_repr           | 497 ms                                                 | 580 ms: 1.17x slower                                                   |
| pprint_pformat             | 1.01 sec                                               | 1.18 sec: 1.17x slower                                                 |
| richards                   | 32.1 ms                                                | 38.1 ms: 1.19x slower                                                  |
| nqueens                    | 62.4 ms                                                | 74.1 ms: 1.19x slower                                                  |
| regex_compile              | 77.9 ms                                                | 92.7 ms: 1.19x slower                                                  |
| comprehensions             | 14.5 us                                                | 17.4 us: 1.19x slower                                                  |
| coverage                   | 38.9 ms                                                | 46.7 ms: 1.20x slower                                                  |
| create_gc_cycles           | 701 us                                                 | 845 us: 1.21x slower                                                   |
| mako                       | 7.71 ms                                                | 9.32 ms: 1.21x slower                                                  |
| tomli_loads                | 1.39 sec                                               | 1.69 sec: 1.21x slower                                                 |
| float                      | 55.8 ms                                                | 69.4 ms: 1.24x slower                                                  |
| unpickle_pure_python       | 151 us                                                 | 188 us: 1.25x slower                                                   |
| nbody                      | 68.8 ms                                                | 86.7 ms: 1.26x slower                                                  |
| scimark_fft                | 195 ms                                                 | 249 ms: 1.28x slower                                                   |
| telco                      | 3.68 ms                                                | 4.80 ms: 1.30x slower                                                  |
| spectral_norm              | 76.4 ms                                                | 102 ms: 1.33x slower                                                   |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 4.19 ms: 1.34x slower                                                  |
| scimark_sor                | 87.4 ms                                                | 117 ms: 1.34x slower                                                   |
| scimark_lu                 | 76.0 ms                                                | 104 ms: 1.36x slower                                                   |
| pyflate                    | 316 ms                                                 | 434 ms: 1.37x slower                                                   |
| hexiom                     | 4.54 ms                                                | 6.31 ms: 1.39x slower                                                  |
| fannkuch                   | 248 ms                                                 | 347 ms: 1.40x slower                                                   |
| scimark_monte_carlo        | 45.0 ms                                                | 65.4 ms: 1.45x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (8): asyncio_tcp, aiohttp, async_generators, sqlglot_normalize, unpickle, xml_etree_parse, dask, gunicorn
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (13) of results/bm-20240329-3.13.0a5+-bfc57d4-PYTHON_UOPS/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.04x