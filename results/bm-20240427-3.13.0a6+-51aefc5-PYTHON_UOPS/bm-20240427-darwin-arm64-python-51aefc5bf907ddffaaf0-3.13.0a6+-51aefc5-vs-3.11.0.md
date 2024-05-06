# Results vs. 3.11.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: darwin-arm64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 180 ms: 1.16x slower                                                   |
| chameleon      | 4.30 ms                                                | 4.76 ms: 1.11x slower                                                  |
| docutils       | 1.43 sec                                               | 1.60 sec: 1.12x slower                                                 |
| html5lib       | 33.0 ms                                                | 32.2 ms: 1.02x faster                                                  |
| tornado_http   | 69.1 ms                                                | 78.6 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 276 ms                                                 | 205 ms: 1.35x faster                                                   |
| async_tree_none            | 282 ms                                                 | 212 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 268 ms: 1.32x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 576 ms: 1.26x faster                                                   |
| async_tree_io              | 697 ms                                                 | 579 ms: 1.20x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 280 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 474 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 473 ms: 1.10x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.24x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| float          | 50.8 ms                                                | 65.0 ms: 1.28x slower                                                  |
| nbody          | 61.7 ms                                                | 84.1 ms: 1.36x slower                                                  |
| Geometric mean | (ref)                                                  | 1.21x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 149 ms: 1.00x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.57 ms: 1.06x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.7 ms: 1.17x slower                                                  |
| regex_compile  | 72.8 ms                                                | 95.1 ms: 1.30x slower                                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.31 ms: 1.19x faster                                                  |
| pickle_pure_python   | 191 us                                                 | 188 us: 1.02x faster                                                   |
| xml_etree_parse      | 100 ms                                                 | 106 ms: 1.05x slower                                                   |
| pickle_dict          | 17.1 us                                                | 18.1 us: 1.06x slower                                                  |
| pickle               | 6.98 us                                                | 7.49 us: 1.07x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.93 us: 1.09x slower                                                  |
| pickle_list          | 2.70 us                                                | 2.96 us: 1.10x slower                                                  |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| unpickle             | 8.29 us                                                | 9.26 us: 1.12x slower                                                  |
| xml_etree_iterparse  | 68.3 ms                                                | 77.4 ms: 1.13x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 40.0 ms: 1.19x slower                                                  |
| unpickle_pure_python | 149 us                                                 | 182 us: 1.22x slower                                                   |
| xml_etree_generate   | 45.8 ms                                                | 58.2 ms: 1.27x slower                                                  |
| tomli_loads          | 1.27 sec                                               | 1.64 sec: 1.29x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 8.57 ms                                                | 10.9 ms: 1.27x slower                                                  |
| python_startup         | 10.8 ms                                                | 13.6 ms: 1.27x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 20.1 ms                                                | 23.1 ms: 1.15x slower                                                  |
| genshi_text     | 14.4 ms                                                | 16.7 ms: 1.16x slower                                                  |
| mako            | 7.93 ms                                                | 9.31 ms: 1.17x slower                                                  |
| genshi_xml      | 28.5 ms                                                | 34.6 ms: 1.21x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.17x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 111 us: 2.72x faster                                                   |
| asyncio_tcp                | 643 ms                                                 | 418 ms: 1.54x faster                                                   |
| pylint                     | 253 ms                                                 | 185 ms: 1.36x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 205 ms: 1.35x faster                                                   |
| async_tree_none            | 282 ms                                                 | 212 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 268 ms: 1.32x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 576 ms: 1.26x faster                                                   |
| async_tree_io              | 697 ms                                                 | 579 ms: 1.20x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 280 ms: 1.20x faster                                                   |
| json_dumps                 | 7.53 ms                                                | 6.31 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 474 ms: 1.16x faster                                                   |
| raytrace                   | 206 ms                                                 | 183 ms: 1.12x faster                                                   |
| generators                 | 30.3 ms                                                | 27.1 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 473 ms: 1.10x faster                                                   |
| sqlglot_parse              | 890 us                                                 | 832 us: 1.07x faster                                                   |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.32 sec: 1.05x faster                                                 |
| sqlglot_transpile          | 1.05 ms                                                | 1.01 ms: 1.05x faster                                                  |
| coroutines                 | 17.2 ms                                                | 16.6 ms: 1.03x faster                                                  |
| logging_simple             | 3.41 us                                                | 3.32 us: 1.03x faster                                                  |
| html5lib                   | 33.0 ms                                                | 32.2 ms: 1.02x faster                                                  |
| logging_format             | 3.67 us                                                | 3.60 us: 1.02x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 188 us: 1.02x faster                                                   |
| logging_silent             | 66.5 ns                                                | 66.6 ns: 1.00x slower                                                  |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.00x slower                                                   |
| chaos                      | 47.4 ms                                                | 47.8 ms: 1.01x slower                                                  |
| pidigits                   | 280 ms                                                 | 283 ms: 1.01x slower                                                   |
| coverage                   | 43.9 ms                                                | 44.8 ms: 1.02x slower                                                  |
| dulwich_log                | 28.6 ms                                                | 29.3 ms: 1.02x slower                                                  |
| sympy_sum                  | 80.2 ms                                                | 82.3 ms: 1.03x slower                                                  |
| pycparser                  | 659 ms                                                 | 678 ms: 1.03x slower                                                   |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                                  |
| dask                       | 219 ms                                                 | 227 ms: 1.04x slower                                                   |
| deltablue                  | 2.75 ms                                                | 2.86 ms: 1.04x slower                                                  |
| deepcopy                   | 215 us                                                 | 225 us: 1.04x slower                                                   |
| pathlib                    | 23.2 ms                                                | 24.2 ms: 1.04x slower                                                  |
| richards_super             | 37.3 ms                                                | 39.0 ms: 1.05x slower                                                  |
| xml_etree_parse            | 100 ms                                                 | 106 ms: 1.05x slower                                                   |
| sympy_integrate            | 11.3 ms                                                | 11.9 ms: 1.05x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.1 us: 1.06x slower                                                  |
| regex_effbot               | 2.43 ms                                                | 2.57 ms: 1.06x slower                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.91 us: 1.06x slower                                                  |
| sympy_expand               | 229 ms                                                 | 245 ms: 1.07x slower                                                   |
| json                       | 2.75 ms                                                | 2.94 ms: 1.07x slower                                                  |
| sympy_str                  | 144 ms                                                 | 154 ms: 1.07x slower                                                   |
| pickle                     | 6.98 us                                                | 7.49 us: 1.07x slower                                                  |
| deepcopy_memo              | 25.7 us                                                | 27.7 us: 1.08x slower                                                  |
| aiohttp                    | 1.02 ms                                                | 1.11 ms: 1.09x slower                                                  |
| unpickle_list              | 2.69 us                                                | 2.93 us: 1.09x slower                                                  |
| thrift                     | 410 us                                                 | 449 us: 1.09x slower                                                   |
| bench_mp_pool              | 41.0 ms                                                | 44.9 ms: 1.10x slower                                                  |
| gunicorn                   | 1.10 ms                                                | 1.20 ms: 1.10x slower                                                  |
| pickle_list                | 2.70 us                                                | 2.96 us: 1.10x slower                                                  |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| chameleon                  | 4.30 ms                                                | 4.76 ms: 1.11x slower                                                  |
| bench_thread_pool          | 465 us                                                 | 516 us: 1.11x slower                                                   |
| unpickle                   | 8.29 us                                                | 9.26 us: 1.12x slower                                                  |
| docutils                   | 1.43 sec                                               | 1.60 sec: 1.12x slower                                                 |
| go                         | 105 ms                                                 | 119 ms: 1.13x slower                                                   |
| meteor_contest             | 71.1 ms                                                | 80.5 ms: 1.13x slower                                                  |
| xml_etree_iterparse        | 68.3 ms                                                | 77.4 ms: 1.13x slower                                                  |
| mdp                        | 1.48 sec                                               | 1.68 sec: 1.13x slower                                                 |
| tornado_http               | 69.1 ms                                                | 78.6 ms: 1.14x slower                                                  |
| richards                   | 31.1 ms                                                | 35.5 ms: 1.14x slower                                                  |
| django_template            | 20.1 ms                                                | 23.1 ms: 1.15x slower                                                  |
| genshi_text                | 14.4 ms                                                | 16.7 ms: 1.16x slower                                                  |
| 2to3                       | 154 ms                                                 | 180 ms: 1.16x slower                                                   |
| sqlglot_normalize          | 162 ms                                                 | 189 ms: 1.17x slower                                                   |
| regex_v8                   | 15.1 ms                                                | 17.7 ms: 1.17x slower                                                  |
| mako                       | 7.93 ms                                                | 9.31 ms: 1.17x slower                                                  |
| crypto_pyaes               | 47.5 ms                                                | 56.4 ms: 1.19x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 40.0 ms: 1.19x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 34.6 ms: 1.21x slower                                                  |
| sqlglot_optimize           | 29.6 ms                                                | 36.2 ms: 1.22x slower                                                  |
| unpickle_pure_python       | 149 us                                                 | 182 us: 1.22x slower                                                   |
| pprint_pformat             | 979 ms                                                 | 1.21 sec: 1.24x slower                                                 |
| pprint_safe_repr           | 478 ms                                                 | 593 ms: 1.24x slower                                                   |
| comprehensions             | 14.4 us                                                | 17.9 us: 1.24x slower                                                  |
| python_startup_no_site     | 8.57 ms                                                | 10.9 ms: 1.27x slower                                                  |
| python_startup             | 10.8 ms                                                | 13.6 ms: 1.27x slower                                                  |
| xml_etree_generate         | 45.8 ms                                                | 58.2 ms: 1.27x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 905 us: 1.27x slower                                                   |
| float                      | 50.8 ms                                                | 65.0 ms: 1.28x slower                                                  |
| nqueens                    | 55.9 ms                                                | 72.1 ms: 1.29x slower                                                  |
| sqlite_synth               | 1.26 us                                                | 1.62 us: 1.29x slower                                                  |
| tomli_loads                | 1.27 sec                                               | 1.64 sec: 1.29x slower                                                 |
| regex_compile              | 72.8 ms                                                | 95.1 ms: 1.30x slower                                                  |
| mypy2                      | 372 ms                                                 | 502 ms: 1.35x slower                                                   |
| hexiom                     | 4.58 ms                                                | 6.19 ms: 1.35x slower                                                  |
| fannkuch                   | 240 ms                                                 | 325 ms: 1.36x slower                                                   |
| nbody                      | 61.7 ms                                                | 84.1 ms: 1.36x slower                                                  |
| scimark_fft                | 173 ms                                                 | 236 ms: 1.37x slower                                                   |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.92 ms: 1.39x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 111 ms: 1.40x slower                                                   |
| spectral_norm              | 65.7 ms                                                | 95.2 ms: 1.45x slower                                                  |
| pyflate                    | 284 ms                                                 | 411 ms: 1.45x slower                                                   |
| scimark_monte_carlo        | 43.5 ms                                                | 63.6 ms: 1.46x slower                                                  |
| telco                      | 3.17 ms                                                | 4.64 ms: 1.46x slower                                                  |
| scimark_lu                 | 67.7 ms                                                | 103 ms: 1.52x slower                                                   |
| async_generators           | 192 ms                                                 | 296 ms: 1.54x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240427-3.13.0a6+-51aefc5-PYTHON_UOPS/bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.08x