# Results vs. 3.11.0

- fork: python
- ref: c43f6a4dfaa1c1974141
- machine: darwin-arm64
- commit hash: c43f6a4
- commit date: 2024-04-03
- overall geometric mean: 1.00x faster
- HPT reliability: 97.89%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 173 ms: 1.12x slower                                                   |
| chameleon      | 4.30 ms                                                | 4.48 ms: 1.04x slower                                                  |
| docutils       | 1.43 sec                                               | 1.56 sec: 1.09x slower                                                 |
| tornado_http   | 69.1 ms                                                | 76.9 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 276 ms                                                 | 197 ms: 1.40x faster                                                   |
| async_tree_none            | 282 ms                                                 | 204 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 261 ms: 1.35x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 562 ms: 1.29x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 261 ms: 1.29x faster                                                   |
| async_tree_io              | 697 ms                                                 | 566 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 467 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 463 ms: 1.12x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 49.1 ms: 1.03x faster                                                  |
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| nbody          | 61.7 ms                                                | 70.5 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 152 ms: 1.03x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.61 ms: 1.08x slower                                                  |
| regex_compile  | 72.8 ms                                                | 80.5 ms: 1.10x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.2 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.39 ms: 1.18x faster                                                  |
| unpickle_pure_python | 149 us                                                 | 141 us: 1.06x faster                                                   |
| pickle_pure_python   | 191 us                                                 | 183 us: 1.05x faster                                                   |
| tomli_loads          | 1.27 sec                                               | 1.29 sec: 1.01x slower                                                 |
| pickle_dict          | 17.1 us                                                | 18.0 us: 1.06x slower                                                  |
| xml_etree_iterparse  | 68.3 ms                                                | 72.3 ms: 1.06x slower                                                  |
| xml_etree_parse      | 100 ms                                                 | 107 ms: 1.06x slower                                                   |
| pickle               | 6.98 us                                                | 7.52 us: 1.08x slower                                                  |
| pickle_list          | 2.70 us                                                | 2.97 us: 1.10x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 37.0 ms: 1.10x slower                                                  |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| unpickle             | 8.29 us                                                | 9.30 us: 1.12x slower                                                  |
| unpickle_list        | 2.69 us                                                | 3.02 us: 1.13x slower                                                  |
| xml_etree_generate   | 45.8 ms                                                | 54.2 ms: 1.18x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 13.4 ms: 1.24x slower                                                  |
| python_startup_no_site | 8.57 ms                                                | 11.6 ms: 1.35x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.30x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 7.93 ms                                                | 6.96 ms: 1.14x faster                                                  |
| genshi_text    | 14.4 ms                                                | 14.7 ms: 1.02x slower                                                  |
| genshi_xml     | 28.5 ms                                                | 31.7 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 69.3 us: 4.34x faster                                                  |
| pylint                     | 253 ms                                                 | 155 ms: 1.63x faster                                                   |
| asyncio_tcp                | 643 ms                                                 | 415 ms: 1.55x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 197 ms: 1.40x faster                                                   |
| async_tree_none            | 282 ms                                                 | 204 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 261 ms: 1.35x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 562 ms: 1.29x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 261 ms: 1.29x faster                                                   |
| chaos                      | 47.4 ms                                                | 38.3 ms: 1.24x faster                                                  |
| async_tree_io              | 697 ms                                                 | 566 ms: 1.23x faster                                                   |
| deltablue                  | 2.75 ms                                                | 2.27 ms: 1.21x faster                                                  |
| comprehensions             | 14.4 us                                                | 12.0 us: 1.20x faster                                                  |
| raytrace                   | 206 ms                                                 | 172 ms: 1.20x faster                                                   |
| json_dumps                 | 7.53 ms                                                | 6.39 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 467 ms: 1.18x faster                                                   |
| generators                 | 30.3 ms                                                | 26.1 ms: 1.16x faster                                                  |
| sqlglot_parse              | 890 us                                                 | 774 us: 1.15x faster                                                   |
| mako                       | 7.93 ms                                                | 6.96 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 463 ms: 1.12x faster                                                   |
| sqlglot_transpile          | 1.05 ms                                                | 940 us: 1.12x faster                                                   |
| logging_simple             | 3.41 us                                                | 3.13 us: 1.09x faster                                                  |
| logging_format             | 3.67 us                                                | 3.41 us: 1.08x faster                                                  |
| richards_super             | 37.3 ms                                                | 35.1 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 149 us                                                 | 141 us: 1.06x faster                                                   |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.32 sec: 1.06x faster                                                 |
| deepcopy_memo              | 25.7 us                                                | 24.4 us: 1.06x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 183 us: 1.05x faster                                                   |
| sympy_sum                  | 80.2 ms                                                | 76.8 ms: 1.04x faster                                                  |
| logging_silent             | 66.5 ns                                                | 63.8 ns: 1.04x faster                                                  |
| float                      | 50.8 ms                                                | 49.1 ms: 1.03x faster                                                  |
| coroutines                 | 17.2 ms                                                | 16.8 ms: 1.02x faster                                                  |
| crypto_pyaes               | 47.5 ms                                                | 46.6 ms: 1.02x faster                                                  |
| sympy_str                  | 144 ms                                                 | 142 ms: 1.02x faster                                                   |
| pycparser                  | 659 ms                                                 | 651 ms: 1.01x faster                                                   |
| deepcopy                   | 215 us                                                 | 214 us: 1.01x faster                                                   |
| scimark_monte_carlo        | 43.5 ms                                                | 43.2 ms: 1.01x faster                                                  |
| asyncio_websockets         | 408 ms                                                 | 410 ms: 1.00x slower                                                   |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| go                         | 105 ms                                                 | 106 ms: 1.01x slower                                                   |
| sympy_integrate            | 11.3 ms                                                | 11.4 ms: 1.01x slower                                                  |
| tomli_loads                | 1.27 sec                                               | 1.29 sec: 1.01x slower                                                 |
| dulwich_log                | 28.6 ms                                                | 29.1 ms: 1.02x slower                                                  |
| genshi_text                | 14.4 ms                                                | 14.7 ms: 1.02x slower                                                  |
| richards                   | 31.1 ms                                                | 31.7 ms: 1.02x slower                                                  |
| regex_dna                  | 148 ms                                                 | 152 ms: 1.03x slower                                                   |
| pprint_safe_repr           | 478 ms                                                 | 493 ms: 1.03x slower                                                   |
| pprint_pformat             | 979 ms                                                 | 1.01 sec: 1.03x slower                                                 |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                                  |
| meteor_contest             | 71.1 ms                                                | 73.5 ms: 1.03x slower                                                  |
| sympy_expand               | 229 ms                                                 | 238 ms: 1.04x slower                                                   |
| chameleon                  | 4.30 ms                                                | 4.48 ms: 1.04x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.88 us: 1.05x slower                                                  |
| aiohttp                    | 1.02 ms                                                | 1.07 ms: 1.05x slower                                                  |
| coverage                   | 43.9 ms                                                | 45.9 ms: 1.05x slower                                                  |
| hexiom                     | 4.58 ms                                                | 4.82 ms: 1.05x slower                                                  |
| bench_thread_pool          | 465 us                                                 | 490 us: 1.05x slower                                                   |
| pickle_dict                | 17.1 us                                                | 18.0 us: 1.06x slower                                                  |
| xml_etree_iterparse        | 68.3 ms                                                | 72.3 ms: 1.06x slower                                                  |
| mdp                        | 1.48 sec                                               | 1.57 sec: 1.06x slower                                                 |
| xml_etree_parse            | 100 ms                                                 | 107 ms: 1.06x slower                                                   |
| thrift                     | 410 us                                                 | 439 us: 1.07x slower                                                   |
| gunicorn                   | 1.10 ms                                                | 1.17 ms: 1.07x slower                                                  |
| pathlib                    | 23.2 ms                                                | 24.9 ms: 1.07x slower                                                  |
| json                       | 2.75 ms                                                | 2.96 ms: 1.07x slower                                                  |
| regex_effbot               | 2.43 ms                                                | 2.61 ms: 1.08x slower                                                  |
| pickle                     | 6.98 us                                                | 7.52 us: 1.08x slower                                                  |
| nqueens                    | 55.9 ms                                                | 60.5 ms: 1.08x slower                                                  |
| fannkuch                   | 240 ms                                                 | 259 ms: 1.08x slower                                                   |
| sqlglot_normalize          | 162 ms                                                 | 176 ms: 1.09x slower                                                   |
| docutils                   | 1.43 sec                                               | 1.56 sec: 1.09x slower                                                 |
| pickle_list                | 2.70 us                                                | 2.97 us: 1.10x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 37.0 ms: 1.10x slower                                                  |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| regex_compile              | 72.8 ms                                                | 80.5 ms: 1.10x slower                                                  |
| mypy2                      | 372 ms                                                 | 412 ms: 1.11x slower                                                   |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.13 ms: 1.11x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 31.7 ms: 1.11x slower                                                  |
| tornado_http               | 69.1 ms                                                | 76.9 ms: 1.11x slower                                                  |
| 2to3                       | 154 ms                                                 | 173 ms: 1.12x slower                                                   |
| spectral_norm              | 65.7 ms                                                | 73.7 ms: 1.12x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.30 us: 1.12x slower                                                  |
| unpickle_list              | 2.69 us                                                | 3.02 us: 1.13x slower                                                  |
| bench_mp_pool              | 41.0 ms                                                | 46.3 ms: 1.13x slower                                                  |
| regex_v8                   | 15.1 ms                                                | 17.2 ms: 1.13x slower                                                  |
| sqlglot_optimize           | 29.6 ms                                                | 33.7 ms: 1.14x slower                                                  |
| pyflate                    | 284 ms                                                 | 324 ms: 1.14x slower                                                   |
| nbody                      | 61.7 ms                                                | 70.5 ms: 1.14x slower                                                  |
| scimark_fft                | 173 ms                                                 | 200 ms: 1.16x slower                                                   |
| xml_etree_generate         | 45.8 ms                                                | 54.2 ms: 1.18x slower                                                  |
| scimark_lu                 | 67.7 ms                                                | 81.7 ms: 1.21x slower                                                  |
| python_startup             | 10.8 ms                                                | 13.4 ms: 1.24x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 896 us: 1.26x slower                                                   |
| sqlite_synth               | 1.26 us                                                | 1.60 us: 1.27x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 106 ms: 1.34x slower                                                   |
| python_startup_no_site     | 8.57 ms                                                | 11.6 ms: 1.35x slower                                                  |
| telco                      | 3.17 ms                                                | 4.51 ms: 1.42x slower                                                  |
| async_generators           | 192 ms                                                 | 302 ms: 1.57x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (2): html5lib, dask
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240403-3.13.0a5+-c43f6a4-JIT/bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 97.89% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x