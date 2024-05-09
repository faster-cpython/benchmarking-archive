# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b1
- machine: darwin-arm64
- commit hash: 2268289
- commit date: 2024-05-08
- overall geometric mean: 1.03x faster
- HPT reliability: 92.24%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 179 ms: 1.16x slower                                       |
| chameleon      | 4.30 ms                                                | 4.35 ms: 1.01x slower                                      |
| docutils       | 1.43 sec                                               | 1.46 sec: 1.02x slower                                     |
| html5lib       | 33.0 ms                                                | 31.2 ms: 1.06x faster                                      |
| Geometric mean | (ref)                                                  | 1.03x slower                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 245 ms: 1.44x faster                                       |
| async_tree_none_tg         | 276 ms                                                 | 197 ms: 1.40x faster                                       |
| async_tree_none            | 282 ms                                                 | 210 ms: 1.34x faster                                       |
| async_tree_memoization     | 336 ms                                                 | 258 ms: 1.30x faster                                       |
| async_tree_io_tg           | 724 ms                                                 | 564 ms: 1.28x faster                                       |
| async_tree_io              | 697 ms                                                 | 570 ms: 1.22x faster                                       |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 453 ms: 1.21x faster                                       |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 469 ms: 1.11x faster                                       |
| Geometric mean             | (ref)                                                  | 1.28x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 50.8 ms                                                | 49.0 ms: 1.04x faster                                      |
| pidigits       | 280 ms                                                 | 282 ms: 1.00x slower                                       |
| nbody          | 61.7 ms                                                | 65.7 ms: 1.07x slower                                      |
| Geometric mean | (ref)                                                  | 1.01x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 68.2 ms: 1.07x faster                                      |
| regex_dna      | 148 ms                                                 | 139 ms: 1.07x faster                                       |
| regex_effbot   | 2.43 ms                                                | 2.55 ms: 1.05x slower                                      |
| regex_v8       | 15.1 ms                                                | 16.8 ms: 1.11x slower                                      |
| Geometric mean | (ref)                                                  | 1.00x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.35 ms: 1.19x faster                                      |
| pickle_pure_python   | 191 us                                                 | 181 us: 1.06x faster                                       |
| unpickle_pure_python | 149 us                                                 | 141 us: 1.05x faster                                       |
| xml_etree_parse      | 100 ms                                                 | 97.6 ms: 1.03x faster                                      |
| xml_etree_iterparse  | 68.3 ms                                                | 67.5 ms: 1.01x faster                                      |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.06x slower                                      |
| pickle               | 6.98 us                                                | 7.47 us: 1.07x slower                                      |
| xml_etree_process    | 33.6 ms                                                | 37.1 ms: 1.10x slower                                      |
| pickle_list          | 2.70 us                                                | 2.98 us: 1.11x slower                                      |
| json_loads           | 15.3 us                                                | 17.3 us: 1.13x slower                                      |
| xml_etree_generate   | 45.8 ms                                                | 51.8 ms: 1.13x slower                                      |
| tomli_loads          | 1.27 sec                                               | 1.45 sec: 1.14x slower                                     |
| unpickle             | 8.29 us                                                | 9.70 us: 1.17x slower                                      |
| unpickle_list        | 2.69 us                                                | 3.31 us: 1.23x slower                                      |
| Geometric mean       | (ref)                                                  | 1.06x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 14.3 ms: 1.33x slower                                      |
| python_startup_no_site | 8.57 ms                                                | 11.6 ms: 1.35x slower                                      |
| Geometric mean         | (ref)                                                  | 1.34x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.88 ms: 1.15x faster                                      |
| genshi_text     | 14.4 ms                                                | 13.8 ms: 1.04x faster                                      |
| django_template | 20.1 ms                                                | 19.4 ms: 1.04x faster                                      |
| genshi_xml      | 28.5 ms                                                | 30.0 ms: 1.05x slower                                      |
| Geometric mean  | (ref)                                                  | 1.04x faster                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 92.5 us: 3.25x faster                                      |
| asyncio_tcp                | 643 ms                                                 | 424 ms: 1.52x faster                                       |
| pylint                     | 253 ms                                                 | 169 ms: 1.50x faster                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 245 ms: 1.44x faster                                       |
| async_tree_none_tg         | 276 ms                                                 | 197 ms: 1.40x faster                                       |
| raytrace                   | 206 ms                                                 | 150 ms: 1.37x faster                                       |
| async_tree_none            | 282 ms                                                 | 210 ms: 1.34x faster                                       |
| generators                 | 30.3 ms                                                | 22.7 ms: 1.34x faster                                      |
| comprehensions             | 14.4 us                                                | 10.9 us: 1.33x faster                                      |
| chaos                      | 47.4 ms                                                | 35.9 ms: 1.32x faster                                      |
| async_tree_memoization     | 336 ms                                                 | 258 ms: 1.30x faster                                       |
| async_tree_io_tg           | 724 ms                                                 | 564 ms: 1.28x faster                                       |
| deltablue                  | 2.75 ms                                                | 2.15 ms: 1.28x faster                                      |
| async_tree_io              | 697 ms                                                 | 570 ms: 1.22x faster                                       |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 453 ms: 1.21x faster                                       |
| sqlglot_parse              | 890 us                                                 | 739 us: 1.20x faster                                       |
| json_dumps                 | 7.53 ms                                                | 6.35 ms: 1.19x faster                                      |
| sqlglot_transpile          | 1.05 ms                                                | 897 us: 1.17x faster                                       |
| mako                       | 7.93 ms                                                | 6.88 ms: 1.15x faster                                      |
| deepcopy_memo              | 25.7 us                                                | 22.4 us: 1.15x faster                                      |
| sympy_sum                  | 80.2 ms                                                | 70.2 ms: 1.14x faster                                      |
| hexiom                     | 4.58 ms                                                | 4.09 ms: 1.12x faster                                      |
| logging_simple             | 3.41 us                                                | 3.06 us: 1.11x faster                                      |
| logging_silent             | 66.5 ns                                                | 60.1 ns: 1.11x faster                                      |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 469 ms: 1.11x faster                                       |
| logging_format             | 3.67 us                                                | 3.36 us: 1.09x faster                                      |
| sympy_integrate            | 11.3 ms                                                | 10.3 ms: 1.09x faster                                      |
| sympy_str                  | 144 ms                                                 | 133 ms: 1.09x faster                                       |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.29 sec: 1.08x faster                                     |
| regex_compile              | 72.8 ms                                                | 68.2 ms: 1.07x faster                                      |
| regex_dna                  | 148 ms                                                 | 139 ms: 1.07x faster                                       |
| coroutines                 | 17.2 ms                                                | 16.2 ms: 1.06x faster                                      |
| deepcopy                   | 215 us                                                 | 203 us: 1.06x faster                                       |
| richards_super             | 37.3 ms                                                | 35.2 ms: 1.06x faster                                      |
| nqueens                    | 55.9 ms                                                | 52.8 ms: 1.06x faster                                      |
| html5lib                   | 33.0 ms                                                | 31.2 ms: 1.06x faster                                      |
| pickle_pure_python         | 191 us                                                 | 181 us: 1.06x faster                                       |
| go                         | 105 ms                                                 | 100 ms: 1.05x faster                                       |
| unpickle_pure_python       | 149 us                                                 | 141 us: 1.05x faster                                       |
| dulwich_log                | 28.6 ms                                                | 27.3 ms: 1.05x faster                                      |
| pycparser                  | 659 ms                                                 | 630 ms: 1.05x faster                                       |
| genshi_text                | 14.4 ms                                                | 13.8 ms: 1.04x faster                                      |
| django_template            | 20.1 ms                                                | 19.4 ms: 1.04x faster                                      |
| float                      | 50.8 ms                                                | 49.0 ms: 1.04x faster                                      |
| pprint_pformat             | 979 ms                                                 | 947 ms: 1.03x faster                                       |
| xml_etree_parse            | 100 ms                                                 | 97.6 ms: 1.03x faster                                      |
| pathlib                    | 23.2 ms                                                | 22.7 ms: 1.02x faster                                      |
| pprint_safe_repr           | 478 ms                                                 | 468 ms: 1.02x faster                                       |
| xml_etree_iterparse        | 68.3 ms                                                | 67.5 ms: 1.01x faster                                      |
| scimark_monte_carlo        | 43.5 ms                                                | 43.0 ms: 1.01x faster                                      |
| meteor_contest             | 71.1 ms                                                | 70.6 ms: 1.01x faster                                      |
| sympy_expand               | 229 ms                                                 | 228 ms: 1.00x faster                                       |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.80 ms: 1.00x faster                                      |
| pidigits                   | 280 ms                                                 | 282 ms: 1.00x slower                                       |
| scimark_lu                 | 67.7 ms                                                | 68.3 ms: 1.01x slower                                      |
| mdp                        | 1.48 sec                                               | 1.50 sec: 1.01x slower                                     |
| chameleon                  | 4.30 ms                                                | 4.35 ms: 1.01x slower                                      |
| docutils                   | 1.43 sec                                               | 1.46 sec: 1.02x slower                                     |
| richards                   | 31.1 ms                                                | 31.9 ms: 1.03x slower                                      |
| sqlglot_normalize          | 162 ms                                                 | 166 ms: 1.03x slower                                       |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                      |
| spectral_norm              | 65.7 ms                                                | 68.2 ms: 1.04x slower                                      |
| sqlglot_optimize           | 29.6 ms                                                | 31.1 ms: 1.05x slower                                      |
| regex_effbot               | 2.43 ms                                                | 2.55 ms: 1.05x slower                                      |
| genshi_xml                 | 28.5 ms                                                | 30.0 ms: 1.05x slower                                      |
| fannkuch                   | 240 ms                                                 | 252 ms: 1.05x slower                                       |
| thrift                     | 410 us                                                 | 434 us: 1.06x slower                                       |
| coverage                   | 43.9 ms                                                | 46.5 ms: 1.06x slower                                      |
| crypto_pyaes               | 47.5 ms                                                | 50.3 ms: 1.06x slower                                      |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.06x slower                                      |
| nbody                      | 61.7 ms                                                | 65.7 ms: 1.07x slower                                      |
| aiohttp                    | 1.02 ms                                                | 1.10 ms: 1.07x slower                                      |
| pickle                     | 6.98 us                                                | 7.47 us: 1.07x slower                                      |
| json                       | 2.75 ms                                                | 2.99 ms: 1.09x slower                                      |
| scimark_fft                | 173 ms                                                 | 190 ms: 1.10x slower                                       |
| bench_mp_pool              | 41.0 ms                                                | 45.2 ms: 1.10x slower                                      |
| xml_etree_process          | 33.6 ms                                                | 37.1 ms: 1.10x slower                                      |
| pickle_list                | 2.70 us                                                | 2.98 us: 1.11x slower                                      |
| regex_v8                   | 15.1 ms                                                | 16.8 ms: 1.11x slower                                      |
| pyflate                    | 284 ms                                                 | 319 ms: 1.13x slower                                       |
| json_loads                 | 15.3 us                                                | 17.3 us: 1.13x slower                                      |
| xml_etree_generate         | 45.8 ms                                                | 51.8 ms: 1.13x slower                                      |
| tomli_loads                | 1.27 sec                                               | 1.45 sec: 1.14x slower                                     |
| 2to3                       | 154 ms                                                 | 179 ms: 1.16x slower                                       |
| unpickle                   | 8.29 us                                                | 9.70 us: 1.17x slower                                      |
| scimark_sor                | 79.2 ms                                                | 96.3 ms: 1.22x slower                                      |
| sqlite_synth               | 1.26 us                                                | 1.54 us: 1.22x slower                                      |
| unpickle_list              | 2.69 us                                                | 3.31 us: 1.23x slower                                      |
| mypy2                      | 372 ms                                                 | 461 ms: 1.24x slower                                       |
| create_gc_cycles           | 711 us                                                 | 884 us: 1.24x slower                                       |
| python_startup             | 10.8 ms                                                | 14.3 ms: 1.33x slower                                      |
| python_startup_no_site     | 8.57 ms                                                | 11.6 ms: 1.35x slower                                      |
| telco                      | 3.17 ms                                                | 4.56 ms: 1.44x slower                                      |
| async_generators           | 192 ms                                                 | 278 ms: 1.45x slower                                       |
| flaskblogging              | 2.35 ms                                                | 5.10 ms: 2.17x slower                                      |
| Geometric mean             | (ref)                                                  | 1.03x faster                                               |

Benchmark hidden because not significant (6): bench_thread_pool, dask, asyncio_websockets, deepcopy_reduce, gunicorn, tornado_http
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-darwin-arm64-python-v3.13.0b1-3.13.0b1-2268289.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 92.24% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x