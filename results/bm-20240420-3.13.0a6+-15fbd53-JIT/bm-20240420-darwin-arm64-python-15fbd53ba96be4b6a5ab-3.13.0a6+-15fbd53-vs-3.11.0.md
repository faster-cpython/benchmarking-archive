# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: darwin-arm64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.02x faster
- HPT reliability: 81.71%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 168 ms: 1.09x slower                                                   |
| chameleon      | 4.30 ms                                                | 4.47 ms: 1.04x slower                                                  |
| docutils       | 1.43 sec                                               | 1.49 sec: 1.05x slower                                                 |
| html5lib       | 33.0 ms                                                | 31.1 ms: 1.06x faster                                                  |
| tornado_http   | 69.1 ms                                                | 76.6 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 276 ms                                                 | 195 ms: 1.42x faster                                                   |
| async_tree_none            | 282 ms                                                 | 201 ms: 1.40x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 259 ms: 1.36x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 553 ms: 1.31x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 268 ms: 1.25x faster                                                   |
| async_tree_io              | 697 ms                                                 | 557 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 465 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 460 ms: 1.13x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 48.6 ms: 1.05x faster                                                  |
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| nbody          | 61.7 ms                                                | 70.1 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.57 ms: 1.06x slower                                                  |
| regex_compile  | 72.8 ms                                                | 83.3 ms: 1.14x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.35 ms: 1.19x faster                                                  |
| unpickle_pure_python | 149 us                                                 | 135 us: 1.10x faster                                                   |
| pickle_pure_python   | 191 us                                                 | 180 us: 1.07x faster                                                   |
| xml_etree_parse      | 100 ms                                                 | 97.8 ms: 1.03x faster                                                  |
| xml_etree_iterparse  | 68.3 ms                                                | 67.7 ms: 1.01x faster                                                  |
| tomli_loads          | 1.27 sec                                               | 1.26 sec: 1.01x faster                                                 |
| pickle_dict          | 17.1 us                                                | 18.1 us: 1.06x slower                                                  |
| pickle               | 6.98 us                                                | 7.43 us: 1.06x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.93 us: 1.09x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 36.7 ms: 1.09x slower                                                  |
| unpickle             | 8.29 us                                                | 9.18 us: 1.11x slower                                                  |
| json_loads           | 15.3 us                                                | 17.0 us: 1.11x slower                                                  |
| pickle_list          | 2.70 us                                                | 3.01 us: 1.12x slower                                                  |
| xml_etree_generate   | 45.8 ms                                                | 52.8 ms: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 8.57 ms                                                | 10.5 ms: 1.22x slower                                                  |
| python_startup         | 10.8 ms                                                | 13.3 ms: 1.24x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.87 ms: 1.16x faster                                                  |
| genshi_text     | 14.4 ms                                                | 14.6 ms: 1.01x slower                                                  |
| django_template | 20.1 ms                                                | 20.4 ms: 1.02x slower                                                  |
| genshi_xml      | 28.5 ms                                                | 30.8 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 68.1 us: 4.42x faster                                                  |
| asyncio_tcp                | 643 ms                                                 | 407 ms: 1.58x faster                                                   |
| pylint                     | 253 ms                                                 | 176 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 195 ms: 1.42x faster                                                   |
| async_tree_none            | 282 ms                                                 | 201 ms: 1.40x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 259 ms: 1.36x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 553 ms: 1.31x faster                                                   |
| raytrace                   | 206 ms                                                 | 163 ms: 1.26x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 268 ms: 1.25x faster                                                   |
| async_tree_io              | 697 ms                                                 | 557 ms: 1.25x faster                                                   |
| chaos                      | 47.4 ms                                                | 37.9 ms: 1.25x faster                                                  |
| comprehensions             | 14.4 us                                                | 11.8 us: 1.22x faster                                                  |
| json_dumps                 | 7.53 ms                                                | 6.35 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 465 ms: 1.18x faster                                                   |
| sqlglot_parse              | 890 us                                                 | 758 us: 1.17x faster                                                   |
| mako                       | 7.93 ms                                                | 6.87 ms: 1.16x faster                                                  |
| generators                 | 30.3 ms                                                | 26.4 ms: 1.15x faster                                                  |
| richards_super             | 37.3 ms                                                | 32.8 ms: 1.14x faster                                                  |
| sqlglot_transpile          | 1.05 ms                                                | 929 us: 1.13x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 460 ms: 1.13x faster                                                   |
| deltablue                  | 2.75 ms                                                | 2.47 ms: 1.11x faster                                                  |
| logging_simple             | 3.41 us                                                | 3.07 us: 1.11x faster                                                  |
| logging_format             | 3.67 us                                                | 3.34 us: 1.10x faster                                                  |
| unpickle_pure_python       | 149 us                                                 | 135 us: 1.10x faster                                                   |
| sympy_sum                  | 80.2 ms                                                | 74.8 ms: 1.07x faster                                                  |
| deepcopy_memo              | 25.7 us                                                | 24.1 us: 1.07x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 180 us: 1.07x faster                                                   |
| html5lib                   | 33.0 ms                                                | 31.1 ms: 1.06x faster                                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.32 sec: 1.06x faster                                                 |
| richards                   | 31.1 ms                                                | 29.5 ms: 1.05x faster                                                  |
| logging_silent             | 66.5 ns                                                | 63.5 ns: 1.05x faster                                                  |
| float                      | 50.8 ms                                                | 48.6 ms: 1.05x faster                                                  |
| sympy_str                  | 144 ms                                                 | 139 ms: 1.03x faster                                                   |
| crypto_pyaes               | 47.5 ms                                                | 46.2 ms: 1.03x faster                                                  |
| xml_etree_parse            | 100 ms                                                 | 97.8 ms: 1.03x faster                                                  |
| pycparser                  | 659 ms                                                 | 645 ms: 1.02x faster                                                   |
| deepcopy                   | 215 us                                                 | 212 us: 1.02x faster                                                   |
| scimark_monte_carlo        | 43.5 ms                                                | 43.0 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 68.3 ms                                                | 67.7 ms: 1.01x faster                                                  |
| tomli_loads                | 1.27 sec                                               | 1.26 sec: 1.01x faster                                                 |
| sympy_integrate            | 11.3 ms                                                | 11.2 ms: 1.01x faster                                                  |
| dulwich_log                | 28.6 ms                                                | 28.4 ms: 1.01x faster                                                  |
| coroutines                 | 17.2 ms                                                | 17.2 ms: 1.00x slower                                                  |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                   |
| go                         | 105 ms                                                 | 106 ms: 1.01x slower                                                   |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| genshi_text                | 14.4 ms                                                | 14.6 ms: 1.01x slower                                                  |
| pathlib                    | 23.2 ms                                                | 23.5 ms: 1.01x slower                                                  |
| django_template            | 20.1 ms                                                | 20.4 ms: 1.02x slower                                                  |
| pprint_safe_repr           | 478 ms                                                 | 486 ms: 1.02x slower                                                   |
| pprint_pformat             | 979 ms                                                 | 995 ms: 1.02x slower                                                   |
| sympy_expand               | 229 ms                                                 | 234 ms: 1.02x slower                                                   |
| gc_traversal               | 2.38 ms                                                | 2.45 ms: 1.03x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.84 us: 1.03x slower                                                  |
| meteor_contest             | 71.1 ms                                                | 73.1 ms: 1.03x slower                                                  |
| hexiom                     | 4.58 ms                                                | 4.71 ms: 1.03x slower                                                  |
| chameleon                  | 4.30 ms                                                | 4.47 ms: 1.04x slower                                                  |
| docutils                   | 1.43 sec                                               | 1.49 sec: 1.05x slower                                                 |
| bench_thread_pool          | 465 us                                                 | 487 us: 1.05x slower                                                   |
| mdp                        | 1.48 sec                                               | 1.57 sec: 1.06x slower                                                 |
| coverage                   | 43.9 ms                                                | 46.4 ms: 1.06x slower                                                  |
| json                       | 2.75 ms                                                | 2.91 ms: 1.06x slower                                                  |
| regex_effbot               | 2.43 ms                                                | 2.57 ms: 1.06x slower                                                  |
| nqueens                    | 55.9 ms                                                | 59.3 ms: 1.06x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.1 us: 1.06x slower                                                  |
| thrift                     | 410 us                                                 | 437 us: 1.06x slower                                                   |
| pickle                     | 6.98 us                                                | 7.43 us: 1.06x slower                                                  |
| sqlglot_normalize          | 162 ms                                                 | 173 ms: 1.07x slower                                                   |
| fannkuch                   | 240 ms                                                 | 258 ms: 1.08x slower                                                   |
| mypy2                      | 372 ms                                                 | 402 ms: 1.08x slower                                                   |
| genshi_xml                 | 28.5 ms                                                | 30.8 ms: 1.08x slower                                                  |
| gunicorn                   | 1.10 ms                                                | 1.19 ms: 1.09x slower                                                  |
| 2to3                       | 154 ms                                                 | 168 ms: 1.09x slower                                                   |
| unpickle_list              | 2.69 us                                                | 2.93 us: 1.09x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 36.7 ms: 1.09x slower                                                  |
| aiohttp                    | 1.02 ms                                                | 1.12 ms: 1.10x slower                                                  |
| pyflate                    | 284 ms                                                 | 314 ms: 1.11x slower                                                   |
| unpickle                   | 8.29 us                                                | 9.18 us: 1.11x slower                                                  |
| tornado_http               | 69.1 ms                                                | 76.6 ms: 1.11x slower                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.12 ms: 1.11x slower                                                  |
| json_loads                 | 15.3 us                                                | 17.0 us: 1.11x slower                                                  |
| pickle_list                | 2.70 us                                                | 3.01 us: 1.12x slower                                                  |
| sqlglot_optimize           | 29.6 ms                                                | 33.1 ms: 1.12x slower                                                  |
| spectral_norm              | 65.7 ms                                                | 73.7 ms: 1.12x slower                                                  |
| bench_mp_pool              | 41.0 ms                                                | 46.2 ms: 1.13x slower                                                  |
| nbody                      | 61.7 ms                                                | 70.1 ms: 1.14x slower                                                  |
| regex_compile              | 72.8 ms                                                | 83.3 ms: 1.14x slower                                                  |
| regex_v8                   | 15.1 ms                                                | 17.4 ms: 1.15x slower                                                  |
| xml_etree_generate         | 45.8 ms                                                | 52.8 ms: 1.15x slower                                                  |
| scimark_fft                | 173 ms                                                 | 201 ms: 1.16x slower                                                   |
| scimark_lu                 | 67.7 ms                                                | 81.6 ms: 1.20x slower                                                  |
| python_startup_no_site     | 8.57 ms                                                | 10.5 ms: 1.22x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 872 us: 1.23x slower                                                   |
| python_startup             | 10.8 ms                                                | 13.3 ms: 1.24x slower                                                  |
| sqlite_synth               | 1.26 us                                                | 1.57 us: 1.25x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 105 ms: 1.33x slower                                                   |
| telco                      | 3.17 ms                                                | 4.58 ms: 1.44x slower                                                  |
| async_generators           | 192 ms                                                 | 296 ms: 1.54x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 81.71% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x