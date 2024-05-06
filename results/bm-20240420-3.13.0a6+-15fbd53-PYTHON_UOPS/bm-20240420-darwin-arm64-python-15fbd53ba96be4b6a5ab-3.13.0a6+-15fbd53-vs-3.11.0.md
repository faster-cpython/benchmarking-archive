# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: darwin-arm64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 172 ms: 1.12x slower                                                   |
| chameleon      | 4.30 ms                                                | 4.68 ms: 1.09x slower                                                  |
| docutils       | 1.43 sec                                               | 1.57 sec: 1.10x slower                                                 |
| html5lib       | 33.0 ms                                                | 32.2 ms: 1.02x faster                                                  |
| tornado_http   | 69.1 ms                                                | 78.8 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 276 ms                                                 | 204 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 265 ms: 1.33x faster                                                   |
| async_tree_none            | 282 ms                                                 | 212 ms: 1.33x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 568 ms: 1.27x faster                                                   |
| async_tree_io              | 697 ms                                                 | 576 ms: 1.21x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 280 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 470 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 472 ms: 1.10x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.24x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| float          | 50.8 ms                                                | 64.7 ms: 1.27x slower                                                  |
| nbody          | 61.7 ms                                                | 83.4 ms: 1.35x slower                                                  |
| Geometric mean | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 149 ms: 1.00x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.63 ms: 1.08x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.6 ms: 1.16x slower                                                  |
| regex_compile  | 72.8 ms                                                | 92.8 ms: 1.27x slower                                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.39 ms: 1.18x faster                                                  |
| pickle_pure_python   | 191 us                                                 | 184 us: 1.04x faster                                                   |
| xml_etree_parse      | 100 ms                                                 | 99.0 ms: 1.01x faster                                                  |
| pickle_dict          | 17.1 us                                                | 18.1 us: 1.06x slower                                                  |
| xml_etree_iterparse  | 68.3 ms                                                | 73.0 ms: 1.07x slower                                                  |
| pickle               | 6.98 us                                                | 7.47 us: 1.07x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.91 us: 1.08x slower                                                  |
| json_loads           | 15.3 us                                                | 17.0 us: 1.11x slower                                                  |
| unpickle             | 8.29 us                                                | 9.21 us: 1.11x slower                                                  |
| pickle_list          | 2.70 us                                                | 3.02 us: 1.12x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 39.1 ms: 1.16x slower                                                  |
| unpickle_pure_python | 149 us                                                 | 181 us: 1.22x slower                                                   |
| xml_etree_generate   | 45.8 ms                                                | 56.8 ms: 1.24x slower                                                  |
| tomli_loads          | 1.27 sec                                               | 1.66 sec: 1.30x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 8.57 ms                                                | 9.19 ms: 1.07x slower                                                  |
| python_startup         | 10.8 ms                                                | 12.0 ms: 1.11x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 14.4 ms                                                | 15.0 ms: 1.04x slower                                                  |
| django_template | 20.1 ms                                                | 22.3 ms: 1.11x slower                                                  |
| genshi_xml      | 28.5 ms                                                | 32.0 ms: 1.12x slower                                                  |
| mako            | 7.93 ms                                                | 9.33 ms: 1.18x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.11x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 71.2 us: 4.22x faster                                                  |
| asyncio_tcp                | 643 ms                                                 | 393 ms: 1.64x faster                                                   |
| pylint                     | 253 ms                                                 | 179 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 204 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 265 ms: 1.33x faster                                                   |
| async_tree_none            | 282 ms                                                 | 212 ms: 1.33x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 568 ms: 1.27x faster                                                   |
| async_tree_io              | 697 ms                                                 | 576 ms: 1.21x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 280 ms: 1.20x faster                                                   |
| json_dumps                 | 7.53 ms                                                | 6.39 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 470 ms: 1.17x faster                                                   |
| generators                 | 30.3 ms                                                | 26.0 ms: 1.17x faster                                                  |
| raytrace                   | 206 ms                                                 | 181 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 472 ms: 1.10x faster                                                   |
| sqlglot_parse              | 890 us                                                 | 833 us: 1.07x faster                                                   |
| logging_simple             | 3.41 us                                                | 3.21 us: 1.06x faster                                                  |
| logging_format             | 3.67 us                                                | 3.47 us: 1.06x faster                                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.32 sec: 1.06x faster                                                 |
| sqlglot_transpile          | 1.05 ms                                                | 1.00 ms: 1.05x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 184 us: 1.04x faster                                                   |
| coroutines                 | 17.2 ms                                                | 16.8 ms: 1.02x faster                                                  |
| html5lib                   | 33.0 ms                                                | 32.2 ms: 1.02x faster                                                  |
| logging_silent             | 66.5 ns                                                | 65.6 ns: 1.01x faster                                                  |
| xml_etree_parse            | 100 ms                                                 | 99.0 ms: 1.01x faster                                                  |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.00x slower                                                   |
| pidigits                   | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| dulwich_log                | 28.6 ms                                                | 28.9 ms: 1.01x slower                                                  |
| sympy_sum                  | 80.2 ms                                                | 81.0 ms: 1.01x slower                                                  |
| dask                       | 219 ms                                                 | 222 ms: 1.01x slower                                                   |
| deepcopy                   | 215 us                                                 | 219 us: 1.02x slower                                                   |
| pycparser                  | 659 ms                                                 | 672 ms: 1.02x slower                                                   |
| deltablue                  | 2.75 ms                                                | 2.81 ms: 1.02x slower                                                  |
| chaos                      | 47.4 ms                                                | 48.4 ms: 1.02x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.45 ms: 1.03x slower                                                  |
| pathlib                    | 23.2 ms                                                | 24.0 ms: 1.04x slower                                                  |
| genshi_text                | 14.4 ms                                                | 15.0 ms: 1.04x slower                                                  |
| sympy_integrate            | 11.3 ms                                                | 11.8 ms: 1.04x slower                                                  |
| richards_super             | 37.3 ms                                                | 39.0 ms: 1.05x slower                                                  |
| sympy_str                  | 144 ms                                                 | 151 ms: 1.05x slower                                                   |
| coverage                   | 43.9 ms                                                | 46.2 ms: 1.05x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.90 us: 1.06x slower                                                  |
| deepcopy_memo              | 25.7 us                                                | 27.3 us: 1.06x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.1 us: 1.06x slower                                                  |
| sympy_expand               | 229 ms                                                 | 244 ms: 1.06x slower                                                   |
| bench_mp_pool              | 41.0 ms                                                | 43.6 ms: 1.06x slower                                                  |
| json                       | 2.75 ms                                                | 2.93 ms: 1.07x slower                                                  |
| xml_etree_iterparse        | 68.3 ms                                                | 73.0 ms: 1.07x slower                                                  |
| pickle                     | 6.98 us                                                | 7.47 us: 1.07x slower                                                  |
| python_startup_no_site     | 8.57 ms                                                | 9.19 ms: 1.07x slower                                                  |
| thrift                     | 410 us                                                 | 443 us: 1.08x slower                                                   |
| bench_thread_pool          | 465 us                                                 | 503 us: 1.08x slower                                                   |
| regex_effbot               | 2.43 ms                                                | 2.63 ms: 1.08x slower                                                  |
| unpickle_list              | 2.69 us                                                | 2.91 us: 1.08x slower                                                  |
| mdp                        | 1.48 sec                                               | 1.61 sec: 1.09x slower                                                 |
| gunicorn                   | 1.10 ms                                                | 1.19 ms: 1.09x slower                                                  |
| chameleon                  | 4.30 ms                                                | 4.68 ms: 1.09x slower                                                  |
| docutils                   | 1.43 sec                                               | 1.57 sec: 1.10x slower                                                 |
| mypy2                      | 372 ms                                                 | 408 ms: 1.10x slower                                                   |
| json_loads                 | 15.3 us                                                | 17.0 us: 1.11x slower                                                  |
| django_template            | 20.1 ms                                                | 22.3 ms: 1.11x slower                                                  |
| meteor_contest             | 71.1 ms                                                | 78.9 ms: 1.11x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.21 us: 1.11x slower                                                  |
| python_startup             | 10.8 ms                                                | 12.0 ms: 1.11x slower                                                  |
| 2to3                       | 154 ms                                                 | 172 ms: 1.12x slower                                                   |
| pickle_list                | 2.70 us                                                | 3.02 us: 1.12x slower                                                  |
| sqlglot_normalize          | 162 ms                                                 | 181 ms: 1.12x slower                                                   |
| genshi_xml                 | 28.5 ms                                                | 32.0 ms: 1.12x slower                                                  |
| aiohttp                    | 1.02 ms                                                | 1.15 ms: 1.12x slower                                                  |
| go                         | 105 ms                                                 | 119 ms: 1.13x slower                                                   |
| tornado_http               | 69.1 ms                                                | 78.8 ms: 1.14x slower                                                  |
| richards                   | 31.1 ms                                                | 35.4 ms: 1.14x slower                                                  |
| comprehensions             | 14.4 us                                                | 16.5 us: 1.14x slower                                                  |
| regex_v8                   | 15.1 ms                                                | 17.6 ms: 1.16x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 39.1 ms: 1.16x slower                                                  |
| mako                       | 7.93 ms                                                | 9.33 ms: 1.18x slower                                                  |
| sqlglot_optimize           | 29.6 ms                                                | 35.2 ms: 1.19x slower                                                  |
| crypto_pyaes               | 47.5 ms                                                | 56.6 ms: 1.19x slower                                                  |
| unpickle_pure_python       | 149 us                                                 | 181 us: 1.22x slower                                                   |
| pprint_safe_repr           | 478 ms                                                 | 587 ms: 1.23x slower                                                   |
| pprint_pformat             | 979 ms                                                 | 1.20 sec: 1.23x slower                                                 |
| create_gc_cycles           | 711 us                                                 | 877 us: 1.23x slower                                                   |
| xml_etree_generate         | 45.8 ms                                                | 56.8 ms: 1.24x slower                                                  |
| nqueens                    | 55.9 ms                                                | 69.9 ms: 1.25x slower                                                  |
| float                      | 50.8 ms                                                | 64.7 ms: 1.27x slower                                                  |
| regex_compile              | 72.8 ms                                                | 92.8 ms: 1.27x slower                                                  |
| sqlite_synth               | 1.26 us                                                | 1.63 us: 1.30x slower                                                  |
| hexiom                     | 4.58 ms                                                | 5.96 ms: 1.30x slower                                                  |
| tomli_loads                | 1.27 sec                                               | 1.66 sec: 1.30x slower                                                 |
| nbody                      | 61.7 ms                                                | 83.4 ms: 1.35x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 112 ms: 1.42x slower                                                   |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 4.00 ms: 1.42x slower                                                  |
| fannkuch                   | 240 ms                                                 | 341 ms: 1.42x slower                                                   |
| scimark_fft                | 173 ms                                                 | 246 ms: 1.43x slower                                                   |
| pyflate                    | 284 ms                                                 | 418 ms: 1.47x slower                                                   |
| scimark_monte_carlo        | 43.5 ms                                                | 64.3 ms: 1.48x slower                                                  |
| telco                      | 3.17 ms                                                | 4.72 ms: 1.49x slower                                                  |
| scimark_lu                 | 67.7 ms                                                | 101 ms: 1.49x slower                                                   |
| spectral_norm              | 65.7 ms                                                | 100 ms: 1.53x slower                                                   |
| async_generators           | 192 ms                                                 | 294 ms: 1.53x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.08x