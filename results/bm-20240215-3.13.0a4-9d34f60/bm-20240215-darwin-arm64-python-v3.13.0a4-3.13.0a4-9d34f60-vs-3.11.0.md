# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a4
- machine: darwin-arm64
- commit hash: 9d34f60
- commit date: 2024-02-15
- overall geometric mean: 1.03x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.44x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 172 ms: 1.11x slower                                       |
| chameleon      | 4.30 ms                                                | 4.81 ms: 1.12x slower                                      |
| docutils       | 1.43 sec                                               | 1.45 sec: 1.02x slower                                     |
| html5lib       | 33.0 ms                                                | 33.9 ms: 1.03x slower                                      |
| Geometric mean | (ref)                                                  | 1.05x slower                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none            | 282 ms                                                 | 253 ms: 1.11x faster                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 324 ms: 1.09x faster                                       |
| async_tree_io_tg           | 724 ms                                                 | 672 ms: 1.08x faster                                       |
| async_tree_none_tg         | 276 ms                                                 | 260 ms: 1.06x faster                                       |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 533 ms: 1.03x faster                                       |
| async_tree_io              | 697 ms                                                 | 704 ms: 1.01x slower                                       |
| Geometric mean             | (ref)                                                  | 1.05x faster                                               |

Benchmark hidden because not significant (2): async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                       |
| float          | 50.8 ms                                                | 56.6 ms: 1.11x slower                                      |
| nbody          | 61.7 ms                                                | 74.3 ms: 1.20x slower                                      |
| Geometric mean | (ref)                                                  | 1.11x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 145 ms: 1.02x faster                                       |
| regex_compile  | 72.8 ms                                                | 73.5 ms: 1.01x slower                                      |
| regex_effbot   | 2.43 ms                                                | 2.48 ms: 1.02x slower                                      |
| regex_v8       | 15.1 ms                                                | 17.1 ms: 1.13x slower                                      |
| Geometric mean | (ref)                                                  | 1.03x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.46 ms: 1.17x faster                                      |
| pickle_pure_python   | 191 us                                                 | 196 us: 1.02x slower                                       |
| pickle               | 6.98 us                                                | 7.22 us: 1.04x slower                                      |
| unpickle_pure_python | 149 us                                                 | 154 us: 1.04x slower                                       |
| xml_etree_parse      | 100 ms                                                 | 105 ms: 1.05x slower                                       |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.06x slower                                      |
| pickle_list          | 2.70 us                                                | 2.89 us: 1.07x slower                                      |
| json_loads           | 15.3 us                                                | 17.0 us: 1.11x slower                                      |
| unpickle             | 8.29 us                                                | 9.22 us: 1.11x slower                                      |
| xml_etree_iterparse  | 68.3 ms                                                | 76.3 ms: 1.12x slower                                      |
| unpickle_list        | 2.69 us                                                | 3.06 us: 1.14x slower                                      |
| xml_etree_process    | 33.6 ms                                                | 39.9 ms: 1.19x slower                                      |
| tomli_loads          | 1.27 sec                                               | 1.55 sec: 1.22x slower                                     |
| xml_etree_generate   | 45.8 ms                                                | 56.2 ms: 1.23x slower                                      |
| Geometric mean       | (ref)                                                  | 1.09x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 12.6 ms: 1.18x slower                                      |
| python_startup_no_site | 8.57 ms                                                | 11.0 ms: 1.28x slower                                      |
| Geometric mean         | (ref)                                                  | 1.23x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| mako            | 7.93 ms                                                | 7.58 ms: 1.05x faster                                      |
| django_template | 20.1 ms                                                | 21.8 ms: 1.08x slower                                      |
| genshi_text     | 14.4 ms                                                | 15.7 ms: 1.09x slower                                      |
| genshi_xml      | 28.5 ms                                                | 33.4 ms: 1.17x slower                                      |
| Geometric mean  | (ref)                                                  | 1.07x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 71.4 us: 4.22x faster                                      |
| asyncio_tcp                | 643 ms                                                 | 410 ms: 1.57x faster                                       |
| pylint                     | 253 ms                                                 | 170 ms: 1.49x faster                                       |
| raytrace                   | 206 ms                                                 | 169 ms: 1.21x faster                                       |
| chaos                      | 47.4 ms                                                | 39.5 ms: 1.20x faster                                      |
| comprehensions             | 14.4 us                                                | 12.1 us: 1.19x faster                                      |
| json_dumps                 | 7.53 ms                                                | 6.46 ms: 1.17x faster                                      |
| deltablue                  | 2.75 ms                                                | 2.43 ms: 1.13x faster                                      |
| sqlglot_parse              | 890 us                                                 | 790 us: 1.13x faster                                       |
| async_tree_none            | 282 ms                                                 | 253 ms: 1.11x faster                                       |
| sympy_sum                  | 80.2 ms                                                | 72.5 ms: 1.11x faster                                      |
| sqlglot_transpile          | 1.05 ms                                                | 964 us: 1.09x faster                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 324 ms: 1.09x faster                                       |
| async_tree_io_tg           | 724 ms                                                 | 672 ms: 1.08x faster                                       |
| async_tree_none_tg         | 276 ms                                                 | 260 ms: 1.06x faster                                       |
| generators                 | 30.3 ms                                                | 28.6 ms: 1.06x faster                                      |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.33 sec: 1.05x faster                                     |
| sympy_integrate            | 11.3 ms                                                | 10.7 ms: 1.05x faster                                      |
| mako                       | 7.93 ms                                                | 7.58 ms: 1.05x faster                                      |
| sympy_str                  | 144 ms                                                 | 139 ms: 1.04x faster                                       |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 533 ms: 1.03x faster                                       |
| regex_dna                  | 148 ms                                                 | 145 ms: 1.02x faster                                       |
| hexiom                     | 4.58 ms                                                | 4.52 ms: 1.01x faster                                      |
| create_gc_cycles           | 711 us                                                 | 707 us: 1.01x faster                                       |
| go                         | 105 ms                                                 | 105 ms: 1.00x faster                                       |
| richards_super             | 37.3 ms                                                | 37.4 ms: 1.00x slower                                      |
| deepcopy_memo              | 25.7 us                                                | 25.8 us: 1.00x slower                                      |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                       |
| gc_traversal               | 2.38 ms                                                | 2.40 ms: 1.01x slower                                      |
| async_tree_io              | 697 ms                                                 | 704 ms: 1.01x slower                                       |
| regex_compile              | 72.8 ms                                                | 73.5 ms: 1.01x slower                                      |
| logging_simple             | 3.41 us                                                | 3.45 us: 1.01x slower                                      |
| docutils                   | 1.43 sec                                               | 1.45 sec: 1.02x slower                                     |
| logging_format             | 3.67 us                                                | 3.74 us: 1.02x slower                                      |
| regex_effbot               | 2.43 ms                                                | 2.48 ms: 1.02x slower                                      |
| crypto_pyaes               | 47.5 ms                                                | 48.5 ms: 1.02x slower                                      |
| dulwich_log                | 28.6 ms                                                | 29.3 ms: 1.02x slower                                      |
| pickle_pure_python         | 191 us                                                 | 196 us: 1.02x slower                                       |
| html5lib                   | 33.0 ms                                                | 33.9 ms: 1.03x slower                                      |
| meteor_contest             | 71.1 ms                                                | 73.0 ms: 1.03x slower                                      |
| pickle                     | 6.98 us                                                | 7.22 us: 1.04x slower                                      |
| unpickle_pure_python       | 149 us                                                 | 154 us: 1.04x slower                                       |
| deepcopy                   | 215 us                                                 | 224 us: 1.04x slower                                       |
| sympy_expand               | 229 ms                                                 | 239 ms: 1.04x slower                                       |
| logging_silent             | 66.5 ns                                                | 69.4 ns: 1.04x slower                                      |
| mdp                        | 1.48 sec                                               | 1.55 sec: 1.05x slower                                     |
| pycparser                  | 659 ms                                                 | 691 ms: 1.05x slower                                       |
| xml_etree_parse            | 100 ms                                                 | 105 ms: 1.05x slower                                       |
| bench_thread_pool          | 465 us                                                 | 492 us: 1.06x slower                                       |
| pathlib                    | 23.2 ms                                                | 24.7 ms: 1.06x slower                                      |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.06x slower                                      |
| pprint_pformat             | 979 ms                                                 | 1.05 sec: 1.07x slower                                     |
| pickle_list                | 2.70 us                                                | 2.89 us: 1.07x slower                                      |
| nqueens                    | 55.9 ms                                                | 60.0 ms: 1.07x slower                                      |
| scimark_monte_carlo        | 43.5 ms                                                | 46.9 ms: 1.08x slower                                      |
| json                       | 2.75 ms                                                | 2.97 ms: 1.08x slower                                      |
| pprint_safe_repr           | 478 ms                                                 | 517 ms: 1.08x slower                                       |
| django_template            | 20.1 ms                                                | 21.8 ms: 1.08x slower                                      |
| richards                   | 31.1 ms                                                | 33.9 ms: 1.09x slower                                      |
| genshi_text                | 14.4 ms                                                | 15.7 ms: 1.09x slower                                      |
| scimark_lu                 | 67.7 ms                                                | 74.6 ms: 1.10x slower                                      |
| bench_mp_pool              | 41.0 ms                                                | 45.2 ms: 1.10x slower                                      |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.11 ms: 1.11x slower                                      |
| deepcopy_reduce            | 1.79 us                                                | 1.98 us: 1.11x slower                                      |
| fannkuch                   | 240 ms                                                 | 265 ms: 1.11x slower                                       |
| json_loads                 | 15.3 us                                                | 17.0 us: 1.11x slower                                      |
| thrift                     | 410 us                                                 | 455 us: 1.11x slower                                       |
| unpickle                   | 8.29 us                                                | 9.22 us: 1.11x slower                                      |
| 2to3                       | 154 ms                                                 | 172 ms: 1.11x slower                                       |
| coroutines                 | 17.2 ms                                                | 19.1 ms: 1.11x slower                                      |
| float                      | 50.8 ms                                                | 56.6 ms: 1.11x slower                                      |
| coverage                   | 43.9 ms                                                | 48.9 ms: 1.11x slower                                      |
| sqlglot_normalize          | 162 ms                                                 | 181 ms: 1.12x slower                                       |
| xml_etree_iterparse        | 68.3 ms                                                | 76.3 ms: 1.12x slower                                      |
| chameleon                  | 4.30 ms                                                | 4.81 ms: 1.12x slower                                      |
| regex_v8                   | 15.1 ms                                                | 17.1 ms: 1.13x slower                                      |
| spectral_norm              | 65.7 ms                                                | 74.7 ms: 1.14x slower                                      |
| unpickle_list              | 2.69 us                                                | 3.06 us: 1.14x slower                                      |
| sqlglot_optimize           | 29.6 ms                                                | 33.8 ms: 1.14x slower                                      |
| gunicorn                   | 1.10 ms                                                | 1.25 ms: 1.14x slower                                      |
| aiohttp                    | 1.02 ms                                                | 1.19 ms: 1.16x slower                                      |
| genshi_xml                 | 28.5 ms                                                | 33.4 ms: 1.17x slower                                      |
| python_startup             | 10.8 ms                                                | 12.6 ms: 1.18x slower                                      |
| scimark_fft                | 173 ms                                                 | 203 ms: 1.18x slower                                       |
| xml_etree_process          | 33.6 ms                                                | 39.9 ms: 1.19x slower                                      |
| pyflate                    | 284 ms                                                 | 338 ms: 1.19x slower                                       |
| nbody                      | 61.7 ms                                                | 74.3 ms: 1.20x slower                                      |
| tomli_loads                | 1.27 sec                                               | 1.55 sec: 1.22x slower                                     |
| mypy2                      | 372 ms                                                 | 456 ms: 1.23x slower                                       |
| xml_etree_generate         | 45.8 ms                                                | 56.2 ms: 1.23x slower                                      |
| sqlite_synth               | 1.26 us                                                | 1.59 us: 1.27x slower                                      |
| python_startup_no_site     | 8.57 ms                                                | 11.0 ms: 1.28x slower                                      |
| scimark_sor                | 79.2 ms                                                | 105 ms: 1.32x slower                                       |
| telco                      | 3.17 ms                                                | 4.49 ms: 1.42x slower                                      |
| flaskblogging              | 2.35 ms                                                | 3.58 ms: 1.52x slower                                      |
| async_generators           | 192 ms                                                 | 298 ms: 1.55x slower                                       |
| Geometric mean             | (ref)                                                  | 1.03x slower                                               |

Benchmark hidden because not significant (4): async_tree_memoization, tornado_http, asyncio_websockets, async_tree_cpu_io_mixed
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240215-3.13.0a4-9d34f60/bm-20240215-darwin-arm64-python-v3.13.0a4-3.13.0a4-9d34f60.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.44x