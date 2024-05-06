# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple
- machine: darwin-arm64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.03x faster
- HPT reliability: 99.45%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 172 ms: 1.01x slower                                                |
| chameleon      | 4.70 ms                                                | 4.50 ms: 1.04x faster                                               |
| docutils       | 1.50 sec                                               | 1.56 sec: 1.04x slower                                              |
| tornado_http   | 69.3 ms                                                | 80.8 ms: 1.17x slower                                               |
| Geometric mean | (ref)                                                  | 1.04x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 258 ms                                                 | 197 ms: 1.31x faster                                                |
| async_tree_none            | 266 ms                                                 | 204 ms: 1.30x faster                                                |
| async_tree_memoization_tg  | 323 ms                                                 | 261 ms: 1.24x faster                                                |
| async_tree_io_tg           | 669 ms                                                 | 561 ms: 1.19x faster                                                |
| async_tree_memoization     | 312 ms                                                 | 263 ms: 1.19x faster                                                |
| async_tree_io              | 668 ms                                                 | 569 ms: 1.17x faster                                                |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 454 ms: 1.17x faster                                                |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 464 ms: 1.13x faster                                                |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 48.9 ms: 1.14x faster                                               |
| nbody          | 68.8 ms                                                | 70.7 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                  | 1.04x faster                                                        |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 154 ms                                                 | 153 ms: 1.01x faster                                                |
| regex_effbot   | 2.64 ms                                                | 2.73 ms: 1.04x slower                                               |
| regex_v8       | 16.0 ms                                                | 17.2 ms: 1.08x slower                                               |
| regex_compile  | 77.9 ms                                                | 84.6 ms: 1.09x slower                                               |
| Geometric mean | (ref)                                                  | 1.05x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 182 us: 1.10x faster                                                |
| tomli_loads          | 1.39 sec                                               | 1.28 sec: 1.09x faster                                              |
| unpickle_pure_python | 151 us                                                 | 141 us: 1.06x faster                                                |
| xml_etree_process    | 39.7 ms                                                | 37.3 ms: 1.06x faster                                               |
| xml_etree_generate   | 55.8 ms                                                | 54.6 ms: 1.02x faster                                               |
| xml_etree_iterparse  | 74.0 ms                                                | 72.6 ms: 1.02x faster                                               |
| json_loads           | 17.2 us                                                | 16.9 us: 1.02x faster                                               |
| pickle_dict          | 18.1 us                                                | 18.1 us: 1.01x slower                                               |
| pickle_list          | 2.89 us                                                | 2.96 us: 1.02x slower                                               |
| json_dumps           | 6.22 ms                                                | 6.38 ms: 1.03x slower                                               |
| pickle               | 7.23 us                                                | 7.44 us: 1.03x slower                                               |
| unpickle             | 9.12 us                                                | 9.62 us: 1.06x slower                                               |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                        |

Benchmark hidden because not significant (2): xml_etree_parse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 11.4 ms                                                | 13.5 ms: 1.18x slower                                               |
| python_startup_no_site | 9.37 ms                                                | 11.7 ms: 1.24x slower                                               |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|-----------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako      | 7.71 ms                                                | 6.95 ms: 1.11x faster                                               |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 93.0 us                                                | 69.7 us: 1.33x faster                                               |
| async_tree_none_tg         | 258 ms                                                 | 197 ms: 1.31x faster                                                |
| raytrace                   | 212 ms                                                 | 163 ms: 1.30x faster                                                |
| async_tree_none            | 266 ms                                                 | 204 ms: 1.30x faster                                                |
| async_tree_memoization_tg  | 323 ms                                                 | 261 ms: 1.24x faster                                                |
| comprehensions             | 14.5 us                                                | 12.1 us: 1.20x faster                                               |
| async_tree_io_tg           | 669 ms                                                 | 561 ms: 1.19x faster                                                |
| async_tree_memoization     | 312 ms                                                 | 263 ms: 1.19x faster                                                |
| generators                 | 31.1 ms                                                | 26.2 ms: 1.19x faster                                               |
| async_tree_io              | 668 ms                                                 | 569 ms: 1.17x faster                                                |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 454 ms: 1.17x faster                                                |
| logging_silent             | 76.4 ns                                                | 65.4 ns: 1.17x faster                                               |
| logging_simple             | 3.69 us                                                | 3.17 us: 1.16x faster                                               |
| logging_format             | 3.98 us                                                | 3.44 us: 1.16x faster                                               |
| deepcopy_memo              | 27.7 us                                                | 24.2 us: 1.14x faster                                               |
| float                      | 55.8 ms                                                | 48.9 ms: 1.14x faster                                               |
| coroutines                 | 19.2 ms                                                | 17.0 ms: 1.13x faster                                               |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 464 ms: 1.13x faster                                                |
| chaos                      | 42.5 ms                                                | 38.0 ms: 1.12x faster                                               |
| sqlglot_parse              | 848 us                                                 | 761 us: 1.11x faster                                                |
| crypto_pyaes               | 51.9 ms                                                | 46.6 ms: 1.11x faster                                               |
| deepcopy_reduce            | 2.07 us                                                | 1.86 us: 1.11x faster                                               |
| mako                       | 7.71 ms                                                | 6.95 ms: 1.11x faster                                               |
| deepcopy                   | 235 us                                                 | 212 us: 1.11x faster                                                |
| asyncio_tcp                | 449 ms                                                 | 405 ms: 1.11x faster                                                |
| pickle_pure_python         | 200 us                                                 | 182 us: 1.10x faster                                                |
| sqlglot_transpile          | 1.02 ms                                                | 931 us: 1.10x faster                                                |
| deltablue                  | 2.71 ms                                                | 2.47 ms: 1.09x faster                                               |
| richards_super             | 36.0 ms                                                | 33.0 ms: 1.09x faster                                               |
| tomli_loads                | 1.39 sec                                               | 1.28 sec: 1.09x faster                                              |
| richards                   | 32.1 ms                                                | 29.7 ms: 1.08x faster                                               |
| unpickle_pure_python       | 151 us                                                 | 141 us: 1.06x faster                                                |
| xml_etree_process          | 39.7 ms                                                | 37.3 ms: 1.06x faster                                               |
| sqlglot_normalize          | 186 ms                                                 | 176 ms: 1.06x faster                                                |
| chameleon                  | 4.70 ms                                                | 4.50 ms: 1.04x faster                                               |
| sympy_str                  | 148 ms                                                 | 143 ms: 1.04x faster                                                |
| pycparser                  | 677 ms                                                 | 654 ms: 1.03x faster                                                |
| dulwich_log                | 29.8 ms                                                | 28.9 ms: 1.03x faster                                               |
| scimark_monte_carlo        | 45.0 ms                                                | 43.7 ms: 1.03x faster                                               |
| nqueens                    | 62.4 ms                                                | 60.6 ms: 1.03x faster                                               |
| bench_thread_pool          | 504 us                                                 | 490 us: 1.03x faster                                                |
| pprint_pformat             | 1.01 sec                                               | 986 ms: 1.03x faster                                                |
| xml_etree_generate         | 55.8 ms                                                | 54.6 ms: 1.02x faster                                               |
| xml_etree_iterparse        | 74.0 ms                                                | 72.6 ms: 1.02x faster                                               |
| pprint_safe_repr           | 497 ms                                                 | 488 ms: 1.02x faster                                                |
| json_loads                 | 17.2 us                                                | 16.9 us: 1.02x faster                                               |
| json                       | 3.09 ms                                                | 3.03 ms: 1.02x faster                                               |
| spectral_norm              | 76.4 ms                                                | 75.1 ms: 1.02x faster                                               |
| async_generators           | 304 ms                                                 | 300 ms: 1.01x faster                                                |
| sympy_expand               | 241 ms                                                 | 238 ms: 1.01x faster                                                |
| regex_dna                  | 154 ms                                                 | 153 ms: 1.01x faster                                                |
| sympy_sum                  | 77.6 ms                                                | 76.8 ms: 1.01x faster                                               |
| sqlglot_optimize           | 34.0 ms                                                | 33.7 ms: 1.01x faster                                               |
| sympy_integrate            | 11.4 ms                                                | 11.4 ms: 1.00x slower                                               |
| pickle_dict                | 18.1 us                                                | 18.1 us: 1.01x slower                                               |
| pyflate                    | 316 ms                                                 | 318 ms: 1.01x slower                                                |
| 2to3                       | 169 ms                                                 | 172 ms: 1.01x slower                                                |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.18 ms: 1.01x slower                                               |
| sqlite_synth               | 1.57 us                                                | 1.59 us: 1.01x slower                                               |
| pickle_list                | 2.89 us                                                | 2.96 us: 1.02x slower                                               |
| gc_traversal               | 2.40 ms                                                | 2.46 ms: 1.02x slower                                               |
| json_dumps                 | 6.22 ms                                                | 6.38 ms: 1.03x slower                                               |
| nbody                      | 68.8 ms                                                | 70.7 ms: 1.03x slower                                               |
| bench_mp_pool              | 44.9 ms                                                | 46.1 ms: 1.03x slower                                               |
| pickle                     | 7.23 us                                                | 7.44 us: 1.03x slower                                               |
| meteor_contest             | 71.7 ms                                                | 74.0 ms: 1.03x slower                                               |
| aiohttp                    | 1.08 ms                                                | 1.12 ms: 1.04x slower                                               |
| regex_effbot               | 2.64 ms                                                | 2.73 ms: 1.04x slower                                               |
| docutils                   | 1.50 sec                                               | 1.56 sec: 1.04x slower                                              |
| scimark_fft                | 195 ms                                                 | 203 ms: 1.04x slower                                                |
| pathlib                    | 24.2 ms                                                | 25.2 ms: 1.04x slower                                               |
| go                         | 102 ms                                                 | 106 ms: 1.05x slower                                                |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.30 sec: 1.05x slower                                              |
| fannkuch                   | 248 ms                                                 | 262 ms: 1.05x slower                                                |
| unpickle                   | 9.12 us                                                | 9.62 us: 1.06x slower                                               |
| hexiom                     | 4.54 ms                                                | 4.82 ms: 1.06x slower                                               |
| gunicorn                   | 1.15 ms                                                | 1.22 ms: 1.06x slower                                               |
| mypy2                      | 380 ms                                                 | 410 ms: 1.08x slower                                                |
| regex_v8                   | 16.0 ms                                                | 17.2 ms: 1.08x slower                                               |
| scimark_lu                 | 76.0 ms                                                | 82.4 ms: 1.08x slower                                               |
| regex_compile              | 77.9 ms                                                | 84.6 ms: 1.09x slower                                               |
| tornado_http               | 69.3 ms                                                | 80.8 ms: 1.17x slower                                               |
| python_startup             | 11.4 ms                                                | 13.5 ms: 1.18x slower                                               |
| coverage                   | 38.9 ms                                                | 46.6 ms: 1.20x slower                                               |
| scimark_sor                | 87.4 ms                                                | 106 ms: 1.22x slower                                                |
| python_startup_no_site     | 9.37 ms                                                | 11.7 ms: 1.24x slower                                               |
| create_gc_cycles           | 701 us                                                 | 900 us: 1.28x slower                                                |
| telco                      | 3.68 ms                                                | 4.75 ms: 1.29x slower                                               |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                        |

Benchmark hidden because not significant (6): dask, xml_etree_parse, asyncio_websockets, mdp, pidigits, unpickle_list
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240405-3.13.0a5+-81bda60-JIT/bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.45% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.24x