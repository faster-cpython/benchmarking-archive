# Results vs. 3.11.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: darwin-arm64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.01x slower
- HPT reliability: 98.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 173 ms: 1.12x slower                                                   |
| chameleon      | 4.30 ms                                                | 4.46 ms: 1.04x slower                                                  |
| docutils       | 1.43 sec                                               | 1.55 sec: 1.09x slower                                                 |
| html5lib       | 33.0 ms                                                | 33.6 ms: 1.02x slower                                                  |
| tornado_http   | 69.1 ms                                                | 79.6 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 249 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 200 ms: 1.38x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 556 ms: 1.30x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 264 ms: 1.27x faster                                                   |
| async_tree_none            | 282 ms                                                 | 226 ms: 1.24x faster                                                   |
| async_tree_io              | 697 ms                                                 | 566 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 459 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 462 ms: 1.12x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 49.2 ms: 1.03x faster                                                  |
| pidigits       | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| nbody          | 61.7 ms                                                | 70.3 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 152 ms: 1.03x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.62 ms: 1.08x slower                                                  |
| regex_compile  | 72.8 ms                                                | 81.0 ms: 1.11x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.1 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.37 ms: 1.18x faster                                                  |
| pickle_pure_python   | 191 us                                                 | 183 us: 1.05x faster                                                   |
| unpickle_pure_python | 149 us                                                 | 143 us: 1.04x faster                                                   |
| tomli_loads          | 1.27 sec                                               | 1.30 sec: 1.02x slower                                                 |
| pickle_dict          | 17.1 us                                                | 18.0 us: 1.06x slower                                                  |
| xml_etree_iterparse  | 68.3 ms                                                | 72.3 ms: 1.06x slower                                                  |
| xml_etree_parse      | 100 ms                                                 | 107 ms: 1.06x slower                                                   |
| pickle               | 6.98 us                                                | 7.44 us: 1.07x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 36.8 ms: 1.10x slower                                                  |
| pickle_list          | 2.70 us                                                | 2.96 us: 1.10x slower                                                  |
| unpickle             | 8.29 us                                                | 9.14 us: 1.10x slower                                                  |
| json_loads           | 15.3 us                                                | 17.0 us: 1.10x slower                                                  |
| unpickle_list        | 2.69 us                                                | 3.05 us: 1.13x slower                                                  |
| xml_etree_generate   | 45.8 ms                                                | 54.4 ms: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 13.4 ms: 1.24x slower                                                  |
| python_startup_no_site | 8.57 ms                                                | 11.6 ms: 1.35x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.30x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.95 ms: 1.14x faster                                                  |
| django_template | 20.1 ms                                                | 20.7 ms: 1.03x slower                                                  |
| genshi_text     | 14.4 ms                                                | 14.9 ms: 1.03x slower                                                  |
| genshi_xml      | 28.5 ms                                                | 31.4 ms: 1.10x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 69.6 us: 4.32x faster                                                  |
| pylint                     | 253 ms                                                 | 156 ms: 1.61x faster                                                   |
| asyncio_tcp                | 643 ms                                                 | 406 ms: 1.58x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 249 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 200 ms: 1.38x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 556 ms: 1.30x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 264 ms: 1.27x faster                                                   |
| async_tree_none            | 282 ms                                                 | 226 ms: 1.24x faster                                                   |
| async_tree_io              | 697 ms                                                 | 566 ms: 1.23x faster                                                   |
| chaos                      | 47.4 ms                                                | 38.5 ms: 1.23x faster                                                  |
| comprehensions             | 14.4 us                                                | 12.0 us: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 459 ms: 1.20x faster                                                   |
| json_dumps                 | 7.53 ms                                                | 6.37 ms: 1.18x faster                                                  |
| deltablue                  | 2.75 ms                                                | 2.36 ms: 1.17x faster                                                  |
| sqlglot_parse              | 890 us                                                 | 765 us: 1.16x faster                                                   |
| generators                 | 30.3 ms                                                | 26.4 ms: 1.15x faster                                                  |
| raytrace                   | 206 ms                                                 | 180 ms: 1.14x faster                                                   |
| mako                       | 7.93 ms                                                | 6.95 ms: 1.14x faster                                                  |
| sqlglot_transpile          | 1.05 ms                                                | 935 us: 1.12x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 462 ms: 1.12x faster                                                   |
| richards_super             | 37.3 ms                                                | 34.9 ms: 1.07x faster                                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.31 sec: 1.06x faster                                                 |
| deepcopy_memo              | 25.7 us                                                | 24.3 us: 1.06x faster                                                  |
| sympy_sum                  | 80.2 ms                                                | 75.9 ms: 1.06x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 183 us: 1.05x faster                                                   |
| unpickle_pure_python       | 149 us                                                 | 143 us: 1.04x faster                                                   |
| logging_simple             | 3.41 us                                                | 3.29 us: 1.04x faster                                                  |
| float                      | 50.8 ms                                                | 49.2 ms: 1.03x faster                                                  |
| coroutines                 | 17.2 ms                                                | 16.7 ms: 1.03x faster                                                  |
| logging_format             | 3.67 us                                                | 3.58 us: 1.03x faster                                                  |
| sympy_str                  | 144 ms                                                 | 140 ms: 1.03x faster                                                   |
| deepcopy                   | 215 us                                                 | 212 us: 1.01x faster                                                   |
| logging_silent             | 66.5 ns                                                | 65.7 ns: 1.01x faster                                                  |
| crypto_pyaes               | 47.5 ms                                                | 47.0 ms: 1.01x faster                                                  |
| go                         | 105 ms                                                 | 105 ms: 1.01x faster                                                   |
| sympy_integrate            | 11.3 ms                                                | 11.3 ms: 1.01x slower                                                  |
| pidigits                   | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| richards                   | 31.1 ms                                                | 31.5 ms: 1.02x slower                                                  |
| scimark_monte_carlo        | 43.5 ms                                                | 44.2 ms: 1.02x slower                                                  |
| tomli_loads                | 1.27 sec                                               | 1.30 sec: 1.02x slower                                                 |
| html5lib                   | 33.0 ms                                                | 33.6 ms: 1.02x slower                                                  |
| pycparser                  | 659 ms                                                 | 671 ms: 1.02x slower                                                   |
| pprint_safe_repr           | 478 ms                                                 | 487 ms: 1.02x slower                                                   |
| pprint_pformat             | 979 ms                                                 | 1.00 sec: 1.02x slower                                                 |
| regex_dna                  | 148 ms                                                 | 152 ms: 1.03x slower                                                   |
| django_template            | 20.1 ms                                                | 20.7 ms: 1.03x slower                                                  |
| sympy_expand               | 229 ms                                                 | 236 ms: 1.03x slower                                                   |
| genshi_text                | 14.4 ms                                                | 14.9 ms: 1.03x slower                                                  |
| chameleon                  | 4.30 ms                                                | 4.46 ms: 1.04x slower                                                  |
| meteor_contest             | 71.1 ms                                                | 74.1 ms: 1.04x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.87 us: 1.04x slower                                                  |
| dulwich_log                | 28.6 ms                                                | 30.0 ms: 1.05x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.0 us: 1.06x slower                                                  |
| mdp                        | 1.48 sec                                               | 1.57 sec: 1.06x slower                                                 |
| xml_etree_iterparse        | 68.3 ms                                                | 72.3 ms: 1.06x slower                                                  |
| bench_thread_pool          | 465 us                                                 | 494 us: 1.06x slower                                                   |
| xml_etree_parse            | 100 ms                                                 | 107 ms: 1.06x slower                                                   |
| coverage                   | 43.9 ms                                                | 46.7 ms: 1.06x slower                                                  |
| thrift                     | 410 us                                                 | 437 us: 1.07x slower                                                   |
| aiohttp                    | 1.02 ms                                                | 1.09 ms: 1.07x slower                                                  |
| pickle                     | 6.98 us                                                | 7.44 us: 1.07x slower                                                  |
| pathlib                    | 23.2 ms                                                | 24.9 ms: 1.07x slower                                                  |
| regex_effbot               | 2.43 ms                                                | 2.62 ms: 1.08x slower                                                  |
| nqueens                    | 55.9 ms                                                | 60.5 ms: 1.08x slower                                                  |
| sqlglot_normalize          | 162 ms                                                 | 175 ms: 1.08x slower                                                   |
| json                       | 2.75 ms                                                | 2.98 ms: 1.08x slower                                                  |
| hexiom                     | 4.58 ms                                                | 4.96 ms: 1.08x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.59 ms: 1.09x slower                                                  |
| docutils                   | 1.43 sec                                               | 1.55 sec: 1.09x slower                                                 |
| fannkuch                   | 240 ms                                                 | 261 ms: 1.09x slower                                                   |
| gunicorn                   | 1.10 ms                                                | 1.20 ms: 1.09x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 36.8 ms: 1.10x slower                                                  |
| pickle_list                | 2.70 us                                                | 2.96 us: 1.10x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 31.4 ms: 1.10x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.14 us: 1.10x slower                                                  |
| json_loads                 | 15.3 us                                                | 17.0 us: 1.10x slower                                                  |
| mypy2                      | 372 ms                                                 | 413 ms: 1.11x slower                                                   |
| regex_compile              | 72.8 ms                                                | 81.0 ms: 1.11x slower                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.13 ms: 1.11x slower                                                  |
| spectral_norm              | 65.7 ms                                                | 73.7 ms: 1.12x slower                                                  |
| 2to3                       | 154 ms                                                 | 173 ms: 1.12x slower                                                   |
| regex_v8                   | 15.1 ms                                                | 17.1 ms: 1.13x slower                                                  |
| bench_mp_pool              | 41.0 ms                                                | 46.4 ms: 1.13x slower                                                  |
| sqlglot_optimize           | 29.6 ms                                                | 33.6 ms: 1.13x slower                                                  |
| unpickle_list              | 2.69 us                                                | 3.05 us: 1.13x slower                                                  |
| nbody                      | 61.7 ms                                                | 70.3 ms: 1.14x slower                                                  |
| tornado_http               | 69.1 ms                                                | 79.6 ms: 1.15x slower                                                  |
| scimark_fft                | 173 ms                                                 | 200 ms: 1.16x slower                                                   |
| pyflate                    | 284 ms                                                 | 332 ms: 1.17x slower                                                   |
| xml_etree_generate         | 45.8 ms                                                | 54.4 ms: 1.19x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 849 us: 1.19x slower                                                   |
| scimark_lu                 | 67.7 ms                                                | 81.6 ms: 1.20x slower                                                  |
| python_startup             | 10.8 ms                                                | 13.4 ms: 1.24x slower                                                  |
| sqlite_synth               | 1.26 us                                                | 1.59 us: 1.27x slower                                                  |
| python_startup_no_site     | 8.57 ms                                                | 11.6 ms: 1.35x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 107 ms: 1.36x slower                                                   |
| telco                      | 3.17 ms                                                | 4.51 ms: 1.42x slower                                                  |
| async_generators           | 192 ms                                                 | 300 ms: 1.56x slower                                                   |
| unpack_sequence            | 33.6 ns                                                | 116 ns: 3.43x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, dask
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (8) of results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 98.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x