# Results vs. 3.11.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: darwin-arm64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.02x faster
- HPT reliability: 92.14%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 165 ms: 1.07x slower                                                   |
| chameleon      | 4.30 ms                                                | 4.60 ms: 1.07x slower                                                  |
| docutils       | 1.43 sec                                               | 1.48 sec: 1.04x slower                                                 |
| html5lib       | 33.0 ms                                                | 34.0 ms: 1.03x slower                                                  |
| tornado_http   | 69.1 ms                                                | 76.3 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 247 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 200 ms: 1.38x faster                                                   |
| async_tree_none            | 282 ms                                                 | 218 ms: 1.29x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 262 ms: 1.28x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 575 ms: 1.26x faster                                                   |
| async_tree_io              | 697 ms                                                 | 558 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 454 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 456 ms: 1.14x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| float          | 50.8 ms                                                | 51.9 ms: 1.02x slower                                                  |
| nbody          | 61.7 ms                                                | 66.1 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 69.7 ms: 1.05x faster                                                  |
| regex_dna      | 148 ms                                                 | 152 ms: 1.03x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.59 ms: 1.07x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.0 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.25 ms: 1.21x faster                                                  |
| pickle_pure_python   | 191 us                                                 | 185 us: 1.03x faster                                                   |
| unpickle_pure_python | 149 us                                                 | 150 us: 1.01x slower                                                   |
| pickle_dict          | 17.1 us                                                | 18.1 us: 1.06x slower                                                  |
| xml_etree_iterparse  | 68.3 ms                                                | 72.8 ms: 1.07x slower                                                  |
| pickle               | 6.98 us                                                | 7.48 us: 1.07x slower                                                  |
| xml_etree_parse      | 100 ms                                                 | 109 ms: 1.08x slower                                                   |
| pickle_list          | 2.70 us                                                | 3.00 us: 1.11x slower                                                  |
| json_loads           | 15.3 us                                                | 17.1 us: 1.12x slower                                                  |
| unpickle             | 8.29 us                                                | 9.27 us: 1.12x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 37.8 ms: 1.13x slower                                                  |
| unpickle_list        | 2.69 us                                                | 3.04 us: 1.13x slower                                                  |
| tomli_loads          | 1.27 sec                                               | 1.49 sec: 1.17x slower                                                 |
| xml_etree_generate   | 45.8 ms                                                | 55.2 ms: 1.21x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 11.9 ms: 1.11x slower                                                  |
| python_startup_no_site | 8.57 ms                                                | 10.2 ms: 1.19x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.95 ms: 1.14x faster                                                  |
| genshi_text     | 14.4 ms                                                | 14.6 ms: 1.01x slower                                                  |
| django_template | 20.1 ms                                                | 20.7 ms: 1.03x slower                                                  |
| genshi_xml      | 28.5 ms                                                | 31.5 ms: 1.11x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 70.8 us: 4.25x faster                                                  |
| pylint                     | 253 ms                                                 | 149 ms: 1.70x faster                                                   |
| asyncio_tcp                | 643 ms                                                 | 417 ms: 1.54x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 247 ms: 1.43x faster                                                   |
| comprehensions             | 14.4 us                                                | 10.2 us: 1.41x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 200 ms: 1.38x faster                                                   |
| raytrace                   | 206 ms                                                 | 157 ms: 1.31x faster                                                   |
| chaos                      | 47.4 ms                                                | 36.5 ms: 1.30x faster                                                  |
| async_tree_none            | 282 ms                                                 | 218 ms: 1.29x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 262 ms: 1.28x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 575 ms: 1.26x faster                                                   |
| unpack_sequence            | 33.6 ns                                                | 26.9 ns: 1.25x faster                                                  |
| async_tree_io              | 697 ms                                                 | 558 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 454 ms: 1.21x faster                                                   |
| json_dumps                 | 7.53 ms                                                | 6.25 ms: 1.21x faster                                                  |
| deltablue                  | 2.75 ms                                                | 2.30 ms: 1.20x faster                                                  |
| sqlglot_parse              | 890 us                                                 | 756 us: 1.18x faster                                                   |
| sympy_sum                  | 80.2 ms                                                | 70.0 ms: 1.15x faster                                                  |
| sqlglot_transpile          | 1.05 ms                                                | 918 us: 1.15x faster                                                   |
| mako                       | 7.93 ms                                                | 6.95 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 456 ms: 1.14x faster                                                   |
| generators                 | 30.3 ms                                                | 27.7 ms: 1.09x faster                                                  |
| sympy_integrate            | 11.3 ms                                                | 10.4 ms: 1.09x faster                                                  |
| sympy_str                  | 144 ms                                                 | 132 ms: 1.09x faster                                                   |
| deepcopy_memo              | 25.7 us                                                | 23.9 us: 1.08x faster                                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.30 sec: 1.08x faster                                                 |
| hexiom                     | 4.58 ms                                                | 4.27 ms: 1.07x faster                                                  |
| richards_super             | 37.3 ms                                                | 34.9 ms: 1.07x faster                                                  |
| go                         | 105 ms                                                 | 101 ms: 1.05x faster                                                   |
| regex_compile              | 72.8 ms                                                | 69.7 ms: 1.05x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 185 us: 1.03x faster                                                   |
| logging_simple             | 3.41 us                                                | 3.34 us: 1.02x faster                                                  |
| logging_format             | 3.67 us                                                | 3.62 us: 1.01x faster                                                  |
| logging_silent             | 66.5 ns                                                | 65.9 ns: 1.01x faster                                                  |
| coroutines                 | 17.2 ms                                                | 17.0 ms: 1.01x faster                                                  |
| crypto_pyaes               | 47.5 ms                                                | 47.2 ms: 1.01x faster                                                  |
| meteor_contest             | 71.1 ms                                                | 71.3 ms: 1.00x slower                                                  |
| nqueens                    | 55.9 ms                                                | 56.2 ms: 1.01x slower                                                  |
| richards                   | 31.1 ms                                                | 31.3 ms: 1.01x slower                                                  |
| dulwich_log                | 28.6 ms                                                | 28.9 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 149 us                                                 | 150 us: 1.01x slower                                                   |
| pidigits                   | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| pprint_pformat             | 979 ms                                                 | 989 ms: 1.01x slower                                                   |
| genshi_text                | 14.4 ms                                                | 14.6 ms: 1.01x slower                                                  |
| pprint_safe_repr           | 478 ms                                                 | 486 ms: 1.02x slower                                                   |
| scimark_lu                 | 67.7 ms                                                | 68.9 ms: 1.02x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.43 ms: 1.02x slower                                                  |
| float                      | 50.8 ms                                                | 51.9 ms: 1.02x slower                                                  |
| bench_thread_pool          | 465 us                                                 | 476 us: 1.02x slower                                                   |
| regex_dna                  | 148 ms                                                 | 152 ms: 1.03x slower                                                   |
| scimark_monte_carlo        | 43.5 ms                                                | 44.6 ms: 1.03x slower                                                  |
| django_template            | 20.1 ms                                                | 20.7 ms: 1.03x slower                                                  |
| mdp                        | 1.48 sec                                               | 1.53 sec: 1.03x slower                                                 |
| html5lib                   | 33.0 ms                                                | 34.0 ms: 1.03x slower                                                  |
| mypy2                      | 372 ms                                                 | 385 ms: 1.03x slower                                                   |
| docutils                   | 1.43 sec                                               | 1.48 sec: 1.04x slower                                                 |
| bench_mp_pool              | 41.0 ms                                                | 42.9 ms: 1.05x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.1 us: 1.06x slower                                                  |
| pathlib                    | 23.2 ms                                                | 24.6 ms: 1.06x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.91 us: 1.06x slower                                                  |
| sqlglot_normalize          | 162 ms                                                 | 172 ms: 1.06x slower                                                   |
| coverage                   | 43.9 ms                                                | 46.8 ms: 1.07x slower                                                  |
| xml_etree_iterparse        | 68.3 ms                                                | 72.8 ms: 1.07x slower                                                  |
| regex_effbot               | 2.43 ms                                                | 2.59 ms: 1.07x slower                                                  |
| 2to3                       | 154 ms                                                 | 165 ms: 1.07x slower                                                   |
| chameleon                  | 4.30 ms                                                | 4.60 ms: 1.07x slower                                                  |
| nbody                      | 61.7 ms                                                | 66.1 ms: 1.07x slower                                                  |
| pickle                     | 6.98 us                                                | 7.48 us: 1.07x slower                                                  |
| thrift                     | 410 us                                                 | 442 us: 1.08x slower                                                   |
| json                       | 2.75 ms                                                | 2.97 ms: 1.08x slower                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.05 ms: 1.08x slower                                                  |
| xml_etree_parse            | 100 ms                                                 | 109 ms: 1.08x slower                                                   |
| sqlglot_optimize           | 29.6 ms                                                | 32.1 ms: 1.08x slower                                                  |
| spectral_norm              | 65.7 ms                                                | 71.3 ms: 1.08x slower                                                  |
| fannkuch                   | 240 ms                                                 | 263 ms: 1.10x slower                                                   |
| tornado_http               | 69.1 ms                                                | 76.3 ms: 1.10x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 31.5 ms: 1.11x slower                                                  |
| python_startup             | 10.8 ms                                                | 11.9 ms: 1.11x slower                                                  |
| pickle_list                | 2.70 us                                                | 3.00 us: 1.11x slower                                                  |
| json_loads                 | 15.3 us                                                | 17.1 us: 1.12x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.27 us: 1.12x slower                                                  |
| regex_v8                   | 15.1 ms                                                | 17.0 ms: 1.12x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 37.8 ms: 1.13x slower                                                  |
| scimark_fft                | 173 ms                                                 | 195 ms: 1.13x slower                                                   |
| unpickle_list              | 2.69 us                                                | 3.04 us: 1.13x slower                                                  |
| pyflate                    | 284 ms                                                 | 329 ms: 1.16x slower                                                   |
| tomli_loads                | 1.27 sec                                               | 1.49 sec: 1.17x slower                                                 |
| create_gc_cycles           | 711 us                                                 | 835 us: 1.17x slower                                                   |
| python_startup_no_site     | 8.57 ms                                                | 10.2 ms: 1.19x slower                                                  |
| xml_etree_generate         | 45.8 ms                                                | 55.2 ms: 1.21x slower                                                  |
| sqlite_synth               | 1.26 us                                                | 1.57 us: 1.25x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 101 ms: 1.27x slower                                                   |
| telco                      | 3.17 ms                                                | 4.54 ms: 1.43x slower                                                  |
| async_generators           | 192 ms                                                 | 286 ms: 1.49x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (7): dask, deepcopy, asyncio_websockets, pycparser, gunicorn, aiohttp, sympy_expand
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (8) of results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 92.14% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x