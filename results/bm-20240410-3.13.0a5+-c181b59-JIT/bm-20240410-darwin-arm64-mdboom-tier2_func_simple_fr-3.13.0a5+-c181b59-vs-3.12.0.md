# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: darwin-arm64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.03x faster
- HPT reliability: 99.80%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 172 ms: 1.02x slower                                                   |
| chameleon      | 4.70 ms                                                | 4.51 ms: 1.04x faster                                                  |
| docutils       | 1.50 sec                                               | 1.56 sec: 1.04x slower                                                 |
| tornado_http   | 69.3 ms                                                | 77.4 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 258 ms                                                 | 197 ms: 1.31x faster                                                   |
| async_tree_none            | 266 ms                                                 | 203 ms: 1.31x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 260 ms: 1.24x faster                                                   |
| async_tree_memoization     | 312 ms                                                 | 261 ms: 1.20x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 561 ms: 1.19x faster                                                   |
| async_tree_io              | 668 ms                                                 | 565 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 454 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 463 ms: 1.13x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 49.3 ms: 1.13x faster                                                  |
| pidigits       | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| nbody          | 68.8 ms                                                | 70.7 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 154 ms                                                 | 152 ms: 1.01x faster                                                   |
| regex_effbot   | 2.64 ms                                                | 2.64 ms: 1.00x faster                                                  |
| regex_v8       | 16.0 ms                                                | 17.1 ms: 1.07x slower                                                  |
| regex_compile  | 77.9 ms                                                | 85.4 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 181 us: 1.10x faster                                                   |
| tomli_loads          | 1.39 sec                                               | 1.28 sec: 1.09x faster                                                 |
| unpickle_pure_python | 151 us                                                 | 141 us: 1.07x faster                                                   |
| xml_etree_process    | 39.7 ms                                                | 37.3 ms: 1.06x faster                                                  |
| xml_etree_generate   | 55.8 ms                                                | 54.6 ms: 1.02x faster                                                  |
| json_loads           | 17.2 us                                                | 16.9 us: 1.02x faster                                                  |
| xml_etree_iterparse  | 74.0 ms                                                | 72.9 ms: 1.02x faster                                                  |
| unpickle_list        | 3.02 us                                                | 2.99 us: 1.01x faster                                                  |
| json_dumps           | 6.22 ms                                                | 6.32 ms: 1.02x slower                                                  |
| pickle_list          | 2.89 us                                                | 2.94 us: 1.02x slower                                                  |
| unpickle             | 9.12 us                                                | 9.32 us: 1.02x slower                                                  |
| pickle               | 7.23 us                                                | 7.46 us: 1.03x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (2): pickle_dict, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.4 ms                                                | 13.6 ms: 1.19x slower                                                  |
| python_startup_no_site | 9.37 ms                                                | 11.8 ms: 1.26x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|-----------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako      | 7.71 ms                                                | 6.96 ms: 1.11x faster                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 93.0 us                                                | 70.0 us: 1.33x faster                                                  |
| async_tree_none_tg         | 258 ms                                                 | 197 ms: 1.31x faster                                                   |
| async_tree_none            | 266 ms                                                 | 203 ms: 1.31x faster                                                   |
| raytrace                   | 212 ms                                                 | 162 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 260 ms: 1.24x faster                                                   |
| comprehensions             | 14.5 us                                                | 12.0 us: 1.21x faster                                                  |
| logging_silent             | 76.4 ns                                                | 63.9 ns: 1.20x faster                                                  |
| async_tree_memoization     | 312 ms                                                 | 261 ms: 1.20x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 561 ms: 1.19x faster                                                   |
| generators                 | 31.1 ms                                                | 26.2 ms: 1.19x faster                                                  |
| async_tree_io              | 668 ms                                                 | 565 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 454 ms: 1.17x faster                                                   |
| logging_simple             | 3.69 us                                                | 3.16 us: 1.17x faster                                                  |
| logging_format             | 3.98 us                                                | 3.44 us: 1.16x faster                                                  |
| deepcopy_memo              | 27.7 us                                                | 24.2 us: 1.14x faster                                                  |
| coroutines                 | 19.2 ms                                                | 16.9 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 463 ms: 1.13x faster                                                   |
| float                      | 55.8 ms                                                | 49.3 ms: 1.13x faster                                                  |
| chaos                      | 42.5 ms                                                | 38.1 ms: 1.12x faster                                                  |
| crypto_pyaes               | 51.9 ms                                                | 46.5 ms: 1.11x faster                                                  |
| mako                       | 7.71 ms                                                | 6.96 ms: 1.11x faster                                                  |
| deepcopy                   | 235 us                                                 | 212 us: 1.11x faster                                                   |
| sqlglot_parse              | 848 us                                                 | 767 us: 1.10x faster                                                   |
| pickle_pure_python         | 200 us                                                 | 181 us: 1.10x faster                                                   |
| deepcopy_reduce            | 2.07 us                                                | 1.88 us: 1.10x faster                                                  |
| deltablue                  | 2.71 ms                                                | 2.48 ms: 1.09x faster                                                  |
| tomli_loads                | 1.39 sec                                               | 1.28 sec: 1.09x faster                                                 |
| richards_super             | 36.0 ms                                                | 33.1 ms: 1.09x faster                                                  |
| sqlglot_transpile          | 1.02 ms                                                | 938 us: 1.09x faster                                                   |
| richards                   | 32.1 ms                                                | 29.8 ms: 1.08x faster                                                  |
| asyncio_tcp                | 449 ms                                                 | 419 ms: 1.07x faster                                                   |
| unpickle_pure_python       | 151 us                                                 | 141 us: 1.07x faster                                                   |
| xml_etree_process          | 39.7 ms                                                | 37.3 ms: 1.06x faster                                                  |
| sqlglot_normalize          | 186 ms                                                 | 176 ms: 1.06x faster                                                   |
| json                       | 3.09 ms                                                | 2.93 ms: 1.05x faster                                                  |
| sympy_str                  | 148 ms                                                 | 142 ms: 1.04x faster                                                   |
| chameleon                  | 4.70 ms                                                | 4.51 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 45.0 ms                                                | 43.3 ms: 1.04x faster                                                  |
| dulwich_log                | 29.8 ms                                                | 28.9 ms: 1.03x faster                                                  |
| bench_thread_pool          | 504 us                                                 | 489 us: 1.03x faster                                                   |
| nqueens                    | 62.4 ms                                                | 60.6 ms: 1.03x faster                                                  |
| pycparser                  | 677 ms                                                 | 658 ms: 1.03x faster                                                   |
| pprint_safe_repr           | 497 ms                                                 | 484 ms: 1.03x faster                                                   |
| spectral_norm              | 76.4 ms                                                | 74.4 ms: 1.03x faster                                                  |
| pprint_pformat             | 1.01 sec                                               | 988 ms: 1.02x faster                                                   |
| xml_etree_generate         | 55.8 ms                                                | 54.6 ms: 1.02x faster                                                  |
| json_loads                 | 17.2 us                                                | 16.9 us: 1.02x faster                                                  |
| xml_etree_iterparse        | 74.0 ms                                                | 72.9 ms: 1.02x faster                                                  |
| async_generators           | 304 ms                                                 | 299 ms: 1.02x faster                                                   |
| regex_dna                  | 154 ms                                                 | 152 ms: 1.01x faster                                                   |
| sympy_expand               | 241 ms                                                 | 238 ms: 1.01x faster                                                   |
| sympy_sum                  | 77.6 ms                                                | 76.6 ms: 1.01x faster                                                  |
| sqlglot_optimize           | 34.0 ms                                                | 33.6 ms: 1.01x faster                                                  |
| unpickle_list              | 3.02 us                                                | 2.99 us: 1.01x faster                                                  |
| mdp                        | 1.58 sec                                               | 1.57 sec: 1.00x faster                                                 |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.12 ms: 1.00x faster                                                  |
| regex_effbot               | 2.64 ms                                                | 2.64 ms: 1.00x faster                                                  |
| pidigits                   | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| sqlite_synth               | 1.57 us                                                | 1.59 us: 1.01x slower                                                  |
| 2to3                       | 169 ms                                                 | 172 ms: 1.02x slower                                                   |
| json_dumps                 | 6.22 ms                                                | 6.32 ms: 1.02x slower                                                  |
| pickle_list                | 2.89 us                                                | 2.94 us: 1.02x slower                                                  |
| unpickle                   | 9.12 us                                                | 9.32 us: 1.02x slower                                                  |
| gc_traversal               | 2.40 ms                                                | 2.46 ms: 1.02x slower                                                  |
| meteor_contest             | 71.7 ms                                                | 73.5 ms: 1.02x slower                                                  |
| scimark_fft                | 195 ms                                                 | 200 ms: 1.03x slower                                                   |
| nbody                      | 68.8 ms                                                | 70.7 ms: 1.03x slower                                                  |
| pathlib                    | 24.2 ms                                                | 24.9 ms: 1.03x slower                                                  |
| bench_mp_pool              | 44.9 ms                                                | 46.2 ms: 1.03x slower                                                  |
| pickle                     | 7.23 us                                                | 7.46 us: 1.03x slower                                                  |
| docutils                   | 1.50 sec                                               | 1.56 sec: 1.04x slower                                                 |
| fannkuch                   | 248 ms                                                 | 258 ms: 1.04x slower                                                   |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.30 sec: 1.05x slower                                                 |
| go                         | 102 ms                                                 | 107 ms: 1.05x slower                                                   |
| hexiom                     | 4.54 ms                                                | 4.84 ms: 1.06x slower                                                  |
| regex_v8                   | 16.0 ms                                                | 17.1 ms: 1.07x slower                                                  |
| mypy2                      | 380 ms                                                 | 409 ms: 1.08x slower                                                   |
| scimark_lu                 | 76.0 ms                                                | 82.1 ms: 1.08x slower                                                  |
| regex_compile              | 77.9 ms                                                | 85.4 ms: 1.10x slower                                                  |
| tornado_http               | 69.3 ms                                                | 77.4 ms: 1.12x slower                                                  |
| python_startup             | 11.4 ms                                                | 13.6 ms: 1.19x slower                                                  |
| coverage                   | 38.9 ms                                                | 46.6 ms: 1.20x slower                                                  |
| scimark_sor                | 87.4 ms                                                | 106 ms: 1.21x slower                                                   |
| telco                      | 3.68 ms                                                | 4.61 ms: 1.25x slower                                                  |
| python_startup_no_site     | 9.37 ms                                                | 11.8 ms: 1.26x slower                                                  |
| create_gc_cycles           | 701 us                                                 | 891 us: 1.27x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (8): dask, pickle_dict, pyflate, asyncio_websockets, sympy_integrate, xml_etree_parse, aiohttp, gunicorn
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240410-3.13.0a5+-c181b59-JIT/bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.80% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x