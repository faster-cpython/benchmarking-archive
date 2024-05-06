# Results vs. 3.11.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: darwin-arm64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 178 ms: 1.15x slower                                                   |
| chameleon      | 4.30 ms                                                | 4.83 ms: 1.12x slower                                                  |
| docutils       | 1.43 sec                                               | 1.62 sec: 1.13x slower                                                 |
| html5lib       | 33.0 ms                                                | 35.0 ms: 1.06x slower                                                  |
| tornado_http   | 69.1 ms                                                | 80.3 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 276 ms                                                 | 209 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 270 ms: 1.31x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 570 ms: 1.27x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 276 ms: 1.22x faster                                                   |
| async_tree_io              | 697 ms                                                 | 584 ms: 1.19x faster                                                   |
| async_tree_none            | 282 ms                                                 | 236 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 464 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 471 ms: 1.10x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| float          | 50.8 ms                                                | 69.4 ms: 1.36x slower                                                  |
| nbody          | 61.7 ms                                                | 86.7 ms: 1.40x slower                                                  |
| Geometric mean | (ref)                                                  | 1.25x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 152 ms: 1.03x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.56 ms: 1.05x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.2 ms: 1.14x slower                                                  |
| regex_compile  | 72.8 ms                                                | 92.7 ms: 1.27x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.28 ms: 1.20x faster                                                  |
| pickle_pure_python   | 191 us                                                 | 189 us: 1.01x faster                                                   |
| pickle_dict          | 17.1 us                                                | 18.1 us: 1.06x slower                                                  |
| xml_etree_parse      | 100 ms                                                 | 107 ms: 1.06x slower                                                   |
| pickle               | 6.98 us                                                | 7.52 us: 1.08x slower                                                  |
| unpickle             | 8.29 us                                                | 9.13 us: 1.10x slower                                                  |
| json_loads           | 15.3 us                                                | 17.0 us: 1.11x slower                                                  |
| pickle_list          | 2.70 us                                                | 3.01 us: 1.12x slower                                                  |
| unpickle_list        | 2.69 us                                                | 3.05 us: 1.14x slower                                                  |
| xml_etree_iterparse  | 68.3 ms                                                | 79.5 ms: 1.16x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 39.2 ms: 1.17x slower                                                  |
| unpickle_pure_python | 149 us                                                 | 188 us: 1.26x slower                                                   |
| xml_etree_generate   | 45.8 ms                                                | 58.9 ms: 1.29x slower                                                  |
| tomli_loads          | 1.27 sec                                               | 1.69 sec: 1.32x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 12.0 ms: 1.11x slower                                                  |
| python_startup_no_site | 8.57 ms                                                | 10.3 ms: 1.20x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 14.4 ms                                                | 15.4 ms: 1.07x slower                                                  |
| django_template | 20.1 ms                                                | 22.6 ms: 1.12x slower                                                  |
| genshi_xml      | 28.5 ms                                                | 33.1 ms: 1.16x slower                                                  |
| mako            | 7.93 ms                                                | 9.32 ms: 1.17x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.13x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 72.6 us: 4.14x faster                                                  |
| pylint                     | 253 ms                                                 | 159 ms: 1.58x faster                                                   |
| asyncio_tcp                | 643 ms                                                 | 436 ms: 1.47x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 209 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 270 ms: 1.31x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 570 ms: 1.27x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 276 ms: 1.22x faster                                                   |
| json_dumps                 | 7.53 ms                                                | 6.28 ms: 1.20x faster                                                  |
| async_tree_io              | 697 ms                                                 | 584 ms: 1.19x faster                                                   |
| async_tree_none            | 282 ms                                                 | 236 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 464 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 471 ms: 1.10x faster                                                   |
| generators                 | 30.3 ms                                                | 28.0 ms: 1.08x faster                                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.31 sec: 1.07x faster                                                 |
| sqlglot_parse              | 890 us                                                 | 843 us: 1.06x faster                                                   |
| deltablue                  | 2.75 ms                                                | 2.63 ms: 1.05x faster                                                  |
| sqlglot_transpile          | 1.05 ms                                                | 1.01 ms: 1.04x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 189 us: 1.01x faster                                                   |
| coroutines                 | 17.2 ms                                                | 17.0 ms: 1.01x faster                                                  |
| logging_simple             | 3.41 us                                                | 3.39 us: 1.01x faster                                                  |
| logging_format             | 3.67 us                                                | 3.68 us: 1.00x slower                                                  |
| pidigits                   | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| chaos                      | 47.4 ms                                                | 48.0 ms: 1.01x slower                                                  |
| dask                       | 219 ms                                                 | 223 ms: 1.02x slower                                                   |
| logging_silent             | 66.5 ns                                                | 67.9 ns: 1.02x slower                                                  |
| sympy_sum                  | 80.2 ms                                                | 82.3 ms: 1.03x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.45 ms: 1.03x slower                                                  |
| regex_dna                  | 148 ms                                                 | 152 ms: 1.03x slower                                                   |
| deepcopy                   | 215 us                                                 | 222 us: 1.03x slower                                                   |
| raytrace                   | 206 ms                                                 | 215 ms: 1.04x slower                                                   |
| aiohttp                    | 1.02 ms                                                | 1.08 ms: 1.05x slower                                                  |
| regex_effbot               | 2.43 ms                                                | 2.56 ms: 1.05x slower                                                  |
| html5lib                   | 33.0 ms                                                | 35.0 ms: 1.06x slower                                                  |
| dulwich_log                | 28.6 ms                                                | 30.4 ms: 1.06x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.1 us: 1.06x slower                                                  |
| xml_etree_parse            | 100 ms                                                 | 107 ms: 1.06x slower                                                   |
| coverage                   | 43.9 ms                                                | 46.7 ms: 1.06x slower                                                  |
| sympy_str                  | 144 ms                                                 | 153 ms: 1.07x slower                                                   |
| unpack_sequence            | 33.6 ns                                                | 35.8 ns: 1.07x slower                                                  |
| sympy_integrate            | 11.3 ms                                                | 12.0 ms: 1.07x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.92 us: 1.07x slower                                                  |
| pycparser                  | 659 ms                                                 | 705 ms: 1.07x slower                                                   |
| bench_mp_pool              | 41.0 ms                                                | 43.8 ms: 1.07x slower                                                  |
| genshi_text                | 14.4 ms                                                | 15.4 ms: 1.07x slower                                                  |
| gunicorn                   | 1.10 ms                                                | 1.18 ms: 1.07x slower                                                  |
| pickle                     | 6.98 us                                                | 7.52 us: 1.08x slower                                                  |
| sympy_expand               | 229 ms                                                 | 247 ms: 1.08x slower                                                   |
| json                       | 2.75 ms                                                | 2.98 ms: 1.08x slower                                                  |
| pathlib                    | 23.2 ms                                                | 25.1 ms: 1.08x slower                                                  |
| deepcopy_memo              | 25.7 us                                                | 28.0 us: 1.09x slower                                                  |
| thrift                     | 410 us                                                 | 447 us: 1.09x slower                                                   |
| unpickle                   | 8.29 us                                                | 9.13 us: 1.10x slower                                                  |
| mdp                        | 1.48 sec                                               | 1.64 sec: 1.10x slower                                                 |
| json_loads                 | 15.3 us                                                | 17.0 us: 1.11x slower                                                  |
| bench_thread_pool          | 465 us                                                 | 517 us: 1.11x slower                                                   |
| python_startup             | 10.8 ms                                                | 12.0 ms: 1.11x slower                                                  |
| pickle_list                | 2.70 us                                                | 3.01 us: 1.12x slower                                                  |
| go                         | 105 ms                                                 | 118 ms: 1.12x slower                                                   |
| mypy2                      | 372 ms                                                 | 417 ms: 1.12x slower                                                   |
| richards_super             | 37.3 ms                                                | 41.8 ms: 1.12x slower                                                  |
| chameleon                  | 4.30 ms                                                | 4.83 ms: 1.12x slower                                                  |
| django_template            | 20.1 ms                                                | 22.6 ms: 1.12x slower                                                  |
| docutils                   | 1.43 sec                                               | 1.62 sec: 1.13x slower                                                 |
| regex_v8                   | 15.1 ms                                                | 17.2 ms: 1.14x slower                                                  |
| unpickle_list              | 2.69 us                                                | 3.05 us: 1.14x slower                                                  |
| meteor_contest             | 71.1 ms                                                | 81.1 ms: 1.14x slower                                                  |
| sqlglot_normalize          | 162 ms                                                 | 186 ms: 1.15x slower                                                   |
| 2to3                       | 154 ms                                                 | 178 ms: 1.15x slower                                                   |
| genshi_xml                 | 28.5 ms                                                | 33.1 ms: 1.16x slower                                                  |
| tornado_http               | 69.1 ms                                                | 80.3 ms: 1.16x slower                                                  |
| xml_etree_iterparse        | 68.3 ms                                                | 79.5 ms: 1.16x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 39.2 ms: 1.17x slower                                                  |
| mako                       | 7.93 ms                                                | 9.32 ms: 1.17x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 845 us: 1.19x slower                                                   |
| crypto_pyaes               | 47.5 ms                                                | 56.7 ms: 1.19x slower                                                  |
| python_startup_no_site     | 8.57 ms                                                | 10.3 ms: 1.20x slower                                                  |
| comprehensions             | 14.4 us                                                | 17.4 us: 1.20x slower                                                  |
| sqlglot_optimize           | 29.6 ms                                                | 35.7 ms: 1.21x slower                                                  |
| pprint_pformat             | 979 ms                                                 | 1.18 sec: 1.21x slower                                                 |
| pprint_safe_repr           | 478 ms                                                 | 580 ms: 1.21x slower                                                   |
| richards                   | 31.1 ms                                                | 38.1 ms: 1.23x slower                                                  |
| unpickle_pure_python       | 149 us                                                 | 188 us: 1.26x slower                                                   |
| regex_compile              | 72.8 ms                                                | 92.7 ms: 1.27x slower                                                  |
| xml_etree_generate         | 45.8 ms                                                | 58.9 ms: 1.29x slower                                                  |
| sqlite_synth               | 1.26 us                                                | 1.65 us: 1.32x slower                                                  |
| tomli_loads                | 1.27 sec                                               | 1.69 sec: 1.32x slower                                                 |
| nqueens                    | 55.9 ms                                                | 74.1 ms: 1.33x slower                                                  |
| float                      | 50.8 ms                                                | 69.4 ms: 1.36x slower                                                  |
| hexiom                     | 4.58 ms                                                | 6.31 ms: 1.38x slower                                                  |
| nbody                      | 61.7 ms                                                | 86.7 ms: 1.40x slower                                                  |
| scimark_fft                | 173 ms                                                 | 249 ms: 1.44x slower                                                   |
| fannkuch                   | 240 ms                                                 | 347 ms: 1.45x slower                                                   |
| scimark_sor                | 79.2 ms                                                | 117 ms: 1.48x slower                                                   |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 4.19 ms: 1.49x slower                                                  |
| scimark_monte_carlo        | 43.5 ms                                                | 65.4 ms: 1.50x slower                                                  |
| telco                      | 3.17 ms                                                | 4.80 ms: 1.51x slower                                                  |
| scimark_lu                 | 67.7 ms                                                | 104 ms: 1.53x slower                                                   |
| pyflate                    | 284 ms                                                 | 434 ms: 1.53x slower                                                   |
| spectral_norm              | 65.7 ms                                                | 102 ms: 1.55x slower                                                   |
| async_generators           | 192 ms                                                 | 303 ms: 1.58x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (8) of results/bm-20240329-3.13.0a5+-bfc57d4-PYTHON_UOPS/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.08x