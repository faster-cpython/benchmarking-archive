# Results vs. 3.12.0

- fork: savannahostrowski
- ref: llvm_18
- machine: darwin-arm64
- commit hash: b2bbeb0
- commit date: 2024-04-27
- overall geometric mean: 1.04x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 183 ms: 1.08x slower                                                 |
| chameleon      | 4.70 ms                                                | 4.45 ms: 1.05x faster                                                |
| docutils       | 1.50 sec                                               | 1.50 sec: 1.00x faster                                               |
| Geometric mean | (ref)                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 266 ms                                                 | 198 ms: 1.34x faster                                                 |
| async_tree_none_tg         | 258 ms                                                 | 195 ms: 1.32x faster                                                 |
| async_tree_memoization_tg  | 323 ms                                                 | 259 ms: 1.25x faster                                                 |
| async_tree_io_tg           | 669 ms                                                 | 558 ms: 1.20x faster                                                 |
| async_tree_io              | 668 ms                                                 | 558 ms: 1.20x faster                                                 |
| async_tree_memoization     | 312 ms                                                 | 268 ms: 1.17x faster                                                 |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 463 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 457 ms: 1.15x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 50.7 ms: 1.10x faster                                                |
| nbody          | 68.8 ms                                                | 67.9 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                  | 1.04x faster                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 77.9 ms                                                | 72.1 ms: 1.08x faster                                                |
| regex_dna      | 154 ms                                                 | 149 ms: 1.03x faster                                                 |
| regex_effbot   | 2.64 ms                                                | 2.58 ms: 1.02x faster                                                |
| regex_v8       | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                |
| Geometric mean | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 151 us                                                 | 132 us: 1.14x faster                                                 |
| tomli_loads          | 1.39 sec                                               | 1.23 sec: 1.13x faster                                               |
| pickle_pure_python   | 200 us                                                 | 182 us: 1.10x faster                                                 |
| xml_etree_process    | 39.7 ms                                                | 36.5 ms: 1.09x faster                                                |
| xml_etree_iterparse  | 74.0 ms                                                | 70.7 ms: 1.05x faster                                                |
| xml_etree_generate   | 55.8 ms                                                | 53.6 ms: 1.04x faster                                                |
| unpickle_list        | 3.02 us                                                | 2.91 us: 1.04x faster                                                |
| xml_etree_parse      | 106 ms                                                 | 104 ms: 1.02x faster                                                 |
| json_loads           | 17.2 us                                                | 17.0 us: 1.01x faster                                                |
| pickle_dict          | 18.1 us                                                | 18.2 us: 1.01x slower                                                |
| json_dumps           | 6.22 ms                                                | 6.31 ms: 1.01x slower                                                |
| unpickle             | 9.12 us                                                | 9.29 us: 1.02x slower                                                |
| pickle_list          | 2.89 us                                                | 2.98 us: 1.03x slower                                                |
| pickle               | 7.23 us                                                | 7.48 us: 1.03x slower                                                |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 9.37 ms                                                | 11.1 ms: 1.19x slower                                                |
| python_startup         | 11.4 ms                                                | 14.1 ms: 1.24x slower                                                |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 7.71 ms                                                | 6.40 ms: 1.21x faster                                                |
| django_template | 22.3 ms                                                | 20.8 ms: 1.08x faster                                                |
| Geometric mean  | (ref)                                                  | 1.14x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 266 ms                                                 | 198 ms: 1.34x faster                                                 |
| async_tree_none_tg         | 258 ms                                                 | 195 ms: 1.32x faster                                                 |
| raytrace                   | 212 ms                                                 | 169 ms: 1.25x faster                                                 |
| async_tree_memoization_tg  | 323 ms                                                 | 259 ms: 1.25x faster                                                 |
| mako                       | 7.71 ms                                                | 6.40 ms: 1.21x faster                                                |
| async_tree_io_tg           | 669 ms                                                 | 558 ms: 1.20x faster                                                 |
| async_tree_io              | 668 ms                                                 | 558 ms: 1.20x faster                                                 |
| logging_silent             | 76.4 ns                                                | 64.2 ns: 1.19x faster                                                |
| logging_simple             | 3.69 us                                                | 3.12 us: 1.18x faster                                                |
| coroutines                 | 19.2 ms                                                | 16.3 ms: 1.18x faster                                                |
| logging_format             | 3.98 us                                                | 3.38 us: 1.18x faster                                                |
| async_tree_memoization     | 312 ms                                                 | 268 ms: 1.17x faster                                                 |
| comprehensions             | 14.5 us                                                | 12.6 us: 1.15x faster                                                |
| generators                 | 31.1 ms                                                | 26.9 ms: 1.15x faster                                                |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 463 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 457 ms: 1.15x faster                                                 |
| deepcopy_memo              | 27.7 us                                                | 24.1 us: 1.15x faster                                                |
| unpickle_pure_python       | 151 us                                                 | 132 us: 1.14x faster                                                 |
| tomli_loads                | 1.39 sec                                               | 1.23 sec: 1.13x faster                                               |
| deltablue                  | 2.71 ms                                                | 2.43 ms: 1.11x faster                                                |
| deepcopy_reduce            | 2.07 us                                                | 1.86 us: 1.11x faster                                                |
| float                      | 55.8 ms                                                | 50.7 ms: 1.10x faster                                                |
| deepcopy                   | 235 us                                                 | 213 us: 1.10x faster                                                 |
| sqlglot_parse              | 848 us                                                 | 772 us: 1.10x faster                                                 |
| pickle_pure_python         | 200 us                                                 | 182 us: 1.10x faster                                                 |
| xml_etree_process          | 39.7 ms                                                | 36.5 ms: 1.09x faster                                                |
| spectral_norm              | 76.4 ms                                                | 70.3 ms: 1.09x faster                                                |
| sqlglot_transpile          | 1.02 ms                                                | 942 us: 1.08x faster                                                 |
| sympy_str                  | 148 ms                                                 | 136 ms: 1.08x faster                                                 |
| regex_compile              | 77.9 ms                                                | 72.1 ms: 1.08x faster                                                |
| richards                   | 32.1 ms                                                | 29.8 ms: 1.08x faster                                                |
| django_template            | 22.3 ms                                                | 20.8 ms: 1.08x faster                                                |
| nqueens                    | 62.4 ms                                                | 58.3 ms: 1.07x faster                                                |
| richards_super             | 36.0 ms                                                | 33.8 ms: 1.07x faster                                                |
| sympy_sum                  | 77.6 ms                                                | 72.8 ms: 1.07x faster                                                |
| json                       | 3.09 ms                                                | 2.91 ms: 1.06x faster                                                |
| crypto_pyaes               | 51.9 ms                                                | 48.9 ms: 1.06x faster                                                |
| chameleon                  | 4.70 ms                                                | 4.45 ms: 1.05x faster                                                |
| sqlglot_normalize          | 186 ms                                                 | 176 ms: 1.05x faster                                                 |
| pycparser                  | 677 ms                                                 | 642 ms: 1.05x faster                                                 |
| fannkuch                   | 248 ms                                                 | 236 ms: 1.05x faster                                                 |
| chaos                      | 42.5 ms                                                | 40.4 ms: 1.05x faster                                                |
| xml_etree_iterparse        | 74.0 ms                                                | 70.7 ms: 1.05x faster                                                |
| pprint_safe_repr           | 497 ms                                                 | 475 ms: 1.05x faster                                                 |
| sympy_integrate            | 11.4 ms                                                | 10.9 ms: 1.05x faster                                                |
| xml_etree_generate         | 55.8 ms                                                | 53.6 ms: 1.04x faster                                                |
| pathlib                    | 24.2 ms                                                | 23.3 ms: 1.04x faster                                                |
| mdp                        | 1.58 sec                                               | 1.52 sec: 1.04x faster                                               |
| sympy_expand               | 241 ms                                                 | 233 ms: 1.04x faster                                                 |
| unpickle_list              | 3.02 us                                                | 2.91 us: 1.04x faster                                                |
| bench_thread_pool          | 504 us                                                 | 487 us: 1.04x faster                                                 |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.03 ms: 1.03x faster                                                |
| dulwich_log                | 29.8 ms                                                | 28.8 ms: 1.03x faster                                                |
| regex_dna                  | 154 ms                                                 | 149 ms: 1.03x faster                                                 |
| async_generators           | 304 ms                                                 | 294 ms: 1.03x faster                                                 |
| pprint_pformat             | 1.01 sec                                               | 980 ms: 1.03x faster                                                 |
| xml_etree_parse            | 106 ms                                                 | 104 ms: 1.02x faster                                                 |
| regex_effbot               | 2.64 ms                                                | 2.58 ms: 1.02x faster                                                |
| sqlglot_optimize           | 34.0 ms                                                | 33.3 ms: 1.02x faster                                                |
| scimark_fft                | 195 ms                                                 | 192 ms: 1.01x faster                                                 |
| hexiom                     | 4.54 ms                                                | 4.48 ms: 1.01x faster                                                |
| nbody                      | 68.8 ms                                                | 67.9 ms: 1.01x faster                                                |
| json_loads                 | 17.2 us                                                | 17.0 us: 1.01x faster                                                |
| scimark_monte_carlo        | 45.0 ms                                                | 44.7 ms: 1.01x faster                                                |
| docutils                   | 1.50 sec                                               | 1.50 sec: 1.00x faster                                               |
| asyncio_websockets         | 409 ms                                                 | 408 ms: 1.00x faster                                                 |
| sqlite_synth               | 1.57 us                                                | 1.57 us: 1.00x faster                                                |
| pyflate                    | 316 ms                                                 | 317 ms: 1.00x slower                                                 |
| pickle_dict                | 18.1 us                                                | 18.2 us: 1.01x slower                                                |
| json_dumps                 | 6.22 ms                                                | 6.31 ms: 1.01x slower                                                |
| meteor_contest             | 71.7 ms                                                | 72.8 ms: 1.01x slower                                                |
| unpickle                   | 9.12 us                                                | 9.29 us: 1.02x slower                                                |
| gc_traversal               | 2.40 ms                                                | 2.46 ms: 1.02x slower                                                |
| go                         | 102 ms                                                 | 104 ms: 1.03x slower                                                 |
| bench_mp_pool              | 44.9 ms                                                | 46.2 ms: 1.03x slower                                                |
| pickle_list                | 2.89 us                                                | 2.98 us: 1.03x slower                                                |
| pickle                     | 7.23 us                                                | 7.48 us: 1.03x slower                                                |
| scimark_lu                 | 76.0 ms                                                | 80.0 ms: 1.05x slower                                                |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.32 sec: 1.06x slower                                               |
| 2to3                       | 169 ms                                                 | 183 ms: 1.08x slower                                                 |
| regex_v8                   | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                |
| typing_runtime_protocols   | 93.0 us                                                | 103 us: 1.11x slower                                                 |
| coverage                   | 38.9 ms                                                | 45.3 ms: 1.17x slower                                                |
| python_startup_no_site     | 9.37 ms                                                | 11.1 ms: 1.19x slower                                                |
| scimark_sor                | 87.4 ms                                                | 104 ms: 1.19x slower                                                 |
| telco                      | 3.68 ms                                                | 4.46 ms: 1.21x slower                                                |
| python_startup             | 11.4 ms                                                | 14.1 ms: 1.24x slower                                                |
| mypy2                      | 380 ms                                                 | 487 ms: 1.28x slower                                                 |
| create_gc_cycles           | 701 us                                                 | 908 us: 1.29x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                         |

Benchmark hidden because not significant (6): asyncio_tcp, dask, pidigits, aiohttp, gunicorn, tornado_http
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240427-3.13.0a6+-b2bbeb0-JIT/bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.26x