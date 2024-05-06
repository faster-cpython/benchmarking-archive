# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: darwin-arm64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.01x faster
- HPT reliability: 90.59%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 171 ms: 1.11x slower                                                   |
| chameleon      | 4.30 ms                                                | 4.46 ms: 1.04x slower                                                  |
| docutils       | 1.43 sec                                               | 1.55 sec: 1.09x slower                                                 |
| tornado_http   | 69.1 ms                                                | 82.6 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 276 ms                                                 | 197 ms: 1.40x faster                                                   |
| async_tree_none            | 282 ms                                                 | 202 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 260 ms: 1.35x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 561 ms: 1.29x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 262 ms: 1.28x faster                                                   |
| async_tree_io              | 697 ms                                                 | 566 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 454 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 463 ms: 1.12x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 49.2 ms: 1.03x faster                                                  |
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| nbody          | 61.7 ms                                                | 70.6 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 152 ms: 1.03x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.64 ms: 1.09x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.1 ms: 1.13x slower                                                  |
| regex_compile  | 72.8 ms                                                | 85.3 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.32 ms: 1.19x faster                                                  |
| unpickle_pure_python | 149 us                                                 | 141 us: 1.06x faster                                                   |
| pickle_pure_python   | 191 us                                                 | 182 us: 1.05x faster                                                   |
| xml_etree_parse      | 100 ms                                                 | 98.5 ms: 1.02x faster                                                  |
| pickle               | 6.98 us                                                | 7.25 us: 1.04x slower                                                  |
| pickle_dict          | 17.1 us                                                | 18.1 us: 1.06x slower                                                  |
| pickle_list          | 2.70 us                                                | 2.95 us: 1.09x slower                                                  |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 37.3 ms: 1.11x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.99 us: 1.11x slower                                                  |
| unpickle             | 8.29 us                                                | 9.27 us: 1.12x slower                                                  |
| xml_etree_generate   | 45.8 ms                                                | 54.4 ms: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (2): tomli_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 13.3 ms: 1.24x slower                                                  |
| python_startup_no_site | 8.57 ms                                                | 11.6 ms: 1.35x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 7.93 ms                                                | 6.93 ms: 1.14x faster                                                  |
| genshi_text    | 14.4 ms                                                | 14.7 ms: 1.02x slower                                                  |
| genshi_xml     | 28.5 ms                                                | 31.5 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 70.4 us: 4.27x faster                                                  |
| pylint                     | 253 ms                                                 | 152 ms: 1.66x faster                                                   |
| asyncio_tcp                | 643 ms                                                 | 410 ms: 1.57x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 197 ms: 1.40x faster                                                   |
| async_tree_none            | 282 ms                                                 | 202 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 260 ms: 1.35x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 561 ms: 1.29x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 262 ms: 1.28x faster                                                   |
| raytrace                   | 206 ms                                                 | 163 ms: 1.26x faster                                                   |
| chaos                      | 47.4 ms                                                | 38.0 ms: 1.25x faster                                                  |
| async_tree_io              | 697 ms                                                 | 566 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 454 ms: 1.21x faster                                                   |
| comprehensions             | 14.4 us                                                | 12.0 us: 1.21x faster                                                  |
| json_dumps                 | 7.53 ms                                                | 6.32 ms: 1.19x faster                                                  |
| generators                 | 30.3 ms                                                | 26.0 ms: 1.16x faster                                                  |
| sqlglot_parse              | 890 us                                                 | 770 us: 1.16x faster                                                   |
| mako                       | 7.93 ms                                                | 6.93 ms: 1.14x faster                                                  |
| richards_super             | 37.3 ms                                                | 32.8 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 463 ms: 1.12x faster                                                   |
| sqlglot_transpile          | 1.05 ms                                                | 943 us: 1.12x faster                                                   |
| deltablue                  | 2.75 ms                                                | 2.47 ms: 1.11x faster                                                  |
| logging_simple             | 3.41 us                                                | 3.14 us: 1.08x faster                                                  |
| logging_format             | 3.67 us                                                | 3.42 us: 1.07x faster                                                  |
| deepcopy_memo              | 25.7 us                                                | 24.1 us: 1.07x faster                                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.31 sec: 1.07x faster                                                 |
| richards                   | 31.1 ms                                                | 29.3 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 149 us                                                 | 141 us: 1.06x faster                                                   |
| pickle_pure_python         | 191 us                                                 | 182 us: 1.05x faster                                                   |
| sympy_sum                  | 80.2 ms                                                | 76.4 ms: 1.05x faster                                                  |
| logging_silent             | 66.5 ns                                                | 63.6 ns: 1.05x faster                                                  |
| float                      | 50.8 ms                                                | 49.2 ms: 1.03x faster                                                  |
| deepcopy                   | 215 us                                                 | 209 us: 1.03x faster                                                   |
| crypto_pyaes               | 47.5 ms                                                | 46.4 ms: 1.02x faster                                                  |
| coroutines                 | 17.2 ms                                                | 16.8 ms: 1.02x faster                                                  |
| xml_etree_parse            | 100 ms                                                 | 98.5 ms: 1.02x faster                                                  |
| sympy_str                  | 144 ms                                                 | 142 ms: 1.02x faster                                                   |
| scimark_monte_carlo        | 43.5 ms                                                | 43.4 ms: 1.00x faster                                                  |
| dulwich_log                | 28.6 ms                                                | 28.8 ms: 1.01x slower                                                  |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| pprint_pformat             | 979 ms                                                 | 987 ms: 1.01x slower                                                   |
| sympy_integrate            | 11.3 ms                                                | 11.4 ms: 1.01x slower                                                  |
| go                         | 105 ms                                                 | 106 ms: 1.01x slower                                                   |
| pprint_safe_repr           | 478 ms                                                 | 488 ms: 1.02x slower                                                   |
| genshi_text                | 14.4 ms                                                | 14.7 ms: 1.02x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.45 ms: 1.03x slower                                                  |
| regex_dna                  | 148 ms                                                 | 152 ms: 1.03x slower                                                   |
| sympy_expand               | 229 ms                                                 | 237 ms: 1.04x slower                                                   |
| chameleon                  | 4.30 ms                                                | 4.46 ms: 1.04x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.86 us: 1.04x slower                                                  |
| pickle                     | 6.98 us                                                | 7.25 us: 1.04x slower                                                  |
| meteor_contest             | 71.1 ms                                                | 74.0 ms: 1.04x slower                                                  |
| bench_thread_pool          | 465 us                                                 | 487 us: 1.05x slower                                                   |
| hexiom                     | 4.58 ms                                                | 4.81 ms: 1.05x slower                                                  |
| coverage                   | 43.9 ms                                                | 46.4 ms: 1.06x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.1 us: 1.06x slower                                                  |
| mdp                        | 1.48 sec                                               | 1.58 sec: 1.06x slower                                                 |
| pathlib                    | 23.2 ms                                                | 24.9 ms: 1.07x slower                                                  |
| json                       | 2.75 ms                                                | 2.96 ms: 1.08x slower                                                  |
| nqueens                    | 55.9 ms                                                | 60.3 ms: 1.08x slower                                                  |
| sqlglot_normalize          | 162 ms                                                 | 175 ms: 1.08x slower                                                   |
| regex_effbot               | 2.43 ms                                                | 2.64 ms: 1.09x slower                                                  |
| docutils                   | 1.43 sec                                               | 1.55 sec: 1.09x slower                                                 |
| fannkuch                   | 240 ms                                                 | 260 ms: 1.09x slower                                                   |
| thrift                     | 410 us                                                 | 447 us: 1.09x slower                                                   |
| aiohttp                    | 1.02 ms                                                | 1.12 ms: 1.09x slower                                                  |
| mypy2                      | 372 ms                                                 | 406 ms: 1.09x slower                                                   |
| pickle_list                | 2.70 us                                                | 2.95 us: 1.09x slower                                                  |
| gunicorn                   | 1.10 ms                                                | 1.20 ms: 1.10x slower                                                  |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 31.5 ms: 1.10x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 37.3 ms: 1.11x slower                                                  |
| pyflate                    | 284 ms                                                 | 315 ms: 1.11x slower                                                   |
| 2to3                       | 154 ms                                                 | 171 ms: 1.11x slower                                                   |
| unpickle_list              | 2.69 us                                                | 2.99 us: 1.11x slower                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.14 ms: 1.11x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.27 us: 1.12x slower                                                  |
| bench_mp_pool              | 41.0 ms                                                | 46.1 ms: 1.13x slower                                                  |
| spectral_norm              | 65.7 ms                                                | 74.3 ms: 1.13x slower                                                  |
| regex_v8                   | 15.1 ms                                                | 17.1 ms: 1.13x slower                                                  |
| sqlglot_optimize           | 29.6 ms                                                | 33.6 ms: 1.13x slower                                                  |
| nbody                      | 61.7 ms                                                | 70.6 ms: 1.14x slower                                                  |
| scimark_fft                | 173 ms                                                 | 200 ms: 1.16x slower                                                   |
| regex_compile              | 72.8 ms                                                | 85.3 ms: 1.17x slower                                                  |
| xml_etree_generate         | 45.8 ms                                                | 54.4 ms: 1.19x slower                                                  |
| tornado_http               | 69.1 ms                                                | 82.6 ms: 1.20x slower                                                  |
| scimark_lu                 | 67.7 ms                                                | 82.0 ms: 1.21x slower                                                  |
| python_startup             | 10.8 ms                                                | 13.3 ms: 1.24x slower                                                  |
| sqlite_synth               | 1.26 us                                                | 1.58 us: 1.26x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 898 us: 1.26x slower                                                   |
| scimark_sor                | 79.2 ms                                                | 106 ms: 1.34x slower                                                   |
| python_startup_no_site     | 8.57 ms                                                | 11.6 ms: 1.35x slower                                                  |
| telco                      | 3.17 ms                                                | 4.60 ms: 1.45x slower                                                  |
| async_generators           | 192 ms                                                 | 299 ms: 1.56x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (6): pycparser, html5lib, asyncio_websockets, tomli_loads, xml_etree_iterparse, dask
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240408-3.13.0a5+-c5564c1-JIT/bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 90.59% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x