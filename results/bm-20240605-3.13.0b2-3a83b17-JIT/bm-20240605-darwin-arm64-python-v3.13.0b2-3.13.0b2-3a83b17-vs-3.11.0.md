# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b2
- machine: darwin-arm64
- commit hash: 3a83b17
- commit date: 2024-06-05
- overall geometric mean: 1.01x faster
- HPT reliability: 51.10%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 173 ms: 1.12x slower                                       |
| chameleon      | 4.30 ms                                                | 4.41 ms: 1.03x slower                                      |
| docutils       | 1.43 sec                                               | 1.51 sec: 1.06x slower                                     |
| html5lib       | 33.0 ms                                                | 31.1 ms: 1.06x faster                                      |
| Geometric mean | (ref)                                                  | 1.03x slower                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 242 ms: 1.45x faster                                       |
| async_tree_none_tg         | 276 ms                                                 | 200 ms: 1.38x faster                                       |
| async_tree_none            | 282 ms                                                 | 212 ms: 1.33x faster                                       |
| async_tree_memoization     | 336 ms                                                 | 263 ms: 1.28x faster                                       |
| async_tree_io_tg           | 724 ms                                                 | 570 ms: 1.27x faster                                       |
| async_tree_io              | 697 ms                                                 | 571 ms: 1.22x faster                                       |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 456 ms: 1.21x faster                                       |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 472 ms: 1.10x faster                                       |
| Geometric mean             | (ref)                                                  | 1.28x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 50.8 ms                                                | 47.4 ms: 1.07x faster                                      |
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                       |
| nbody          | 61.7 ms                                                | 63.5 ms: 1.03x slower                                      |
| Geometric mean | (ref)                                                  | 1.01x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 71.9 ms: 1.01x faster                                      |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                       |
| regex_effbot   | 2.43 ms                                                | 2.58 ms: 1.06x slower                                      |
| regex_v8       | 15.1 ms                                                | 17.3 ms: 1.14x slower                                      |
| Geometric mean | (ref)                                                  | 1.05x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.17 ms: 1.22x faster                                      |
| unpickle_pure_python | 149 us                                                 | 132 us: 1.13x faster                                       |
| pickle_pure_python   | 191 us                                                 | 173 us: 1.11x faster                                       |
| tomli_loads          | 1.27 sec                                               | 1.24 sec: 1.03x faster                                     |
| xml_etree_iterparse  | 68.3 ms                                                | 70.5 ms: 1.03x slower                                      |
| xml_etree_parse      | 100 ms                                                 | 105 ms: 1.05x slower                                       |
| xml_etree_process    | 33.6 ms                                                | 35.8 ms: 1.07x slower                                      |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.07x slower                                      |
| unpickle_list        | 2.69 us                                                | 2.88 us: 1.07x slower                                      |
| pickle               | 6.98 us                                                | 7.52 us: 1.08x slower                                      |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                      |
| pickle_list          | 2.70 us                                                | 2.99 us: 1.11x slower                                      |
| unpickle             | 8.29 us                                                | 9.19 us: 1.11x slower                                      |
| xml_etree_generate   | 45.8 ms                                                | 51.6 ms: 1.13x slower                                      |
| Geometric mean       | (ref)                                                  | 1.02x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 16.4 ms: 1.52x slower                                      |
| python_startup_no_site | 8.57 ms                                                | 13.4 ms: 1.57x slower                                      |
| Geometric mean         | (ref)                                                  | 1.54x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.40 ms: 1.24x faster                                      |
| django_template | 20.1 ms                                                | 21.3 ms: 1.06x slower                                      |
| genshi_text     | 14.4 ms                                                | 16.4 ms: 1.14x slower                                      |
| genshi_xml      | 28.5 ms                                                | 39.3 ms: 1.38x slower                                      |
| Geometric mean  | (ref)                                                  | 1.08x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 93.5 us: 3.22x faster                                      |
| asyncio_tcp                | 643 ms                                                 | 417 ms: 1.54x faster                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 242 ms: 1.45x faster                                       |
| pylint                     | 253 ms                                                 | 183 ms: 1.38x faster                                       |
| async_tree_none_tg         | 276 ms                                                 | 200 ms: 1.38x faster                                       |
| async_tree_none            | 282 ms                                                 | 212 ms: 1.33x faster                                       |
| generators                 | 30.3 ms                                                | 23.6 ms: 1.29x faster                                      |
| async_tree_memoization     | 336 ms                                                 | 263 ms: 1.28x faster                                       |
| async_tree_io_tg           | 724 ms                                                 | 570 ms: 1.27x faster                                       |
| raytrace                   | 206 ms                                                 | 163 ms: 1.26x faster                                       |
| mako                       | 7.93 ms                                                | 6.40 ms: 1.24x faster                                      |
| async_tree_io              | 697 ms                                                 | 571 ms: 1.22x faster                                       |
| json_dumps                 | 7.53 ms                                                | 6.17 ms: 1.22x faster                                      |
| chaos                      | 47.4 ms                                                | 38.9 ms: 1.22x faster                                      |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 456 ms: 1.21x faster                                       |
| deepcopy_memo              | 25.7 us                                                | 21.5 us: 1.20x faster                                      |
| comprehensions             | 14.4 us                                                | 12.2 us: 1.18x faster                                      |
| logging_simple             | 3.41 us                                                | 3.02 us: 1.13x faster                                      |
| unpickle_pure_python       | 149 us                                                 | 132 us: 1.13x faster                                       |
| deltablue                  | 2.75 ms                                                | 2.47 ms: 1.11x faster                                      |
| sympy_sum                  | 80.2 ms                                                | 72.4 ms: 1.11x faster                                      |
| pickle_pure_python         | 191 us                                                 | 173 us: 1.11x faster                                       |
| logging_format             | 3.67 us                                                | 3.33 us: 1.10x faster                                      |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 472 ms: 1.10x faster                                       |
| sqlglot_parse              | 890 us                                                 | 826 us: 1.08x faster                                       |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.30 sec: 1.08x faster                                     |
| float                      | 50.8 ms                                                | 47.4 ms: 1.07x faster                                      |
| coroutines                 | 17.2 ms                                                | 16.0 ms: 1.07x faster                                      |
| html5lib                   | 33.0 ms                                                | 31.1 ms: 1.06x faster                                      |
| logging_silent             | 66.5 ns                                                | 63.1 ns: 1.05x faster                                      |
| hexiom                     | 4.58 ms                                                | 4.36 ms: 1.05x faster                                      |
| sqlglot_transpile          | 1.05 ms                                                | 1.00 ms: 1.05x faster                                      |
| sympy_str                  | 144 ms                                                 | 137 ms: 1.05x faster                                       |
| richards_super             | 37.3 ms                                                | 35.7 ms: 1.05x faster                                      |
| mdp                        | 1.48 sec                                               | 1.43 sec: 1.04x faster                                     |
| deepcopy                   | 215 us                                                 | 208 us: 1.04x faster                                       |
| sympy_integrate            | 11.3 ms                                                | 10.9 ms: 1.03x faster                                      |
| go                         | 105 ms                                                 | 102 ms: 1.03x faster                                       |
| pprint_safe_repr           | 478 ms                                                 | 464 ms: 1.03x faster                                       |
| fannkuch                   | 240 ms                                                 | 233 ms: 1.03x faster                                       |
| tomli_loads                | 1.27 sec                                               | 1.24 sec: 1.03x faster                                     |
| pprint_pformat             | 979 ms                                                 | 958 ms: 1.02x faster                                       |
| regex_compile              | 72.8 ms                                                | 71.9 ms: 1.01x faster                                      |
| asyncio_websockets         | 408 ms                                                 | 409 ms: 1.00x slower                                       |
| meteor_contest             | 71.1 ms                                                | 71.4 ms: 1.01x slower                                      |
| dulwich_log                | 28.6 ms                                                | 28.8 ms: 1.01x slower                                      |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                       |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                       |
| scimark_monte_carlo        | 43.5 ms                                                | 44.0 ms: 1.01x slower                                      |
| deepcopy_reduce            | 1.79 us                                                | 1.82 us: 1.02x slower                                      |
| nqueens                    | 55.9 ms                                                | 56.8 ms: 1.02x slower                                      |
| pycparser                  | 659 ms                                                 | 672 ms: 1.02x slower                                       |
| dask                       | 219 ms                                                 | 223 ms: 1.02x slower                                       |
| richards                   | 31.1 ms                                                | 31.7 ms: 1.02x slower                                      |
| coverage                   | 43.9 ms                                                | 44.9 ms: 1.02x slower                                      |
| spectral_norm              | 65.7 ms                                                | 67.5 ms: 1.03x slower                                      |
| chameleon                  | 4.30 ms                                                | 4.41 ms: 1.03x slower                                      |
| nbody                      | 61.7 ms                                                | 63.5 ms: 1.03x slower                                      |
| sympy_expand               | 229 ms                                                 | 236 ms: 1.03x slower                                       |
| bench_thread_pool          | 465 us                                                 | 481 us: 1.03x slower                                       |
| xml_etree_iterparse        | 68.3 ms                                                | 70.5 ms: 1.03x slower                                      |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                      |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.92 ms: 1.04x slower                                      |
| gunicorn                   | 1.10 ms                                                | 1.15 ms: 1.05x slower                                      |
| xml_etree_parse            | 100 ms                                                 | 105 ms: 1.05x slower                                       |
| docutils                   | 1.43 sec                                               | 1.51 sec: 1.06x slower                                     |
| django_template            | 20.1 ms                                                | 21.3 ms: 1.06x slower                                      |
| regex_effbot               | 2.43 ms                                                | 2.58 ms: 1.06x slower                                      |
| json                       | 2.75 ms                                                | 2.93 ms: 1.07x slower                                      |
| xml_etree_process          | 33.6 ms                                                | 35.8 ms: 1.07x slower                                      |
| thrift                     | 410 us                                                 | 438 us: 1.07x slower                                       |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.07x slower                                      |
| unpickle_list              | 2.69 us                                                | 2.88 us: 1.07x slower                                      |
| scimark_fft                | 173 ms                                                 | 185 ms: 1.07x slower                                       |
| aiohttp                    | 1.02 ms                                                | 1.10 ms: 1.07x slower                                      |
| pickle                     | 6.98 us                                                | 7.52 us: 1.08x slower                                      |
| crypto_pyaes               | 47.5 ms                                                | 51.8 ms: 1.09x slower                                      |
| mypy2                      | 372 ms                                                 | 408 ms: 1.10x slower                                       |
| sqlglot_optimize           | 29.6 ms                                                | 32.6 ms: 1.10x slower                                      |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                      |
| pickle_list                | 2.70 us                                                | 2.99 us: 1.11x slower                                      |
| unpickle                   | 8.29 us                                                | 9.19 us: 1.11x slower                                      |
| pyflate                    | 284 ms                                                 | 315 ms: 1.11x slower                                       |
| 2to3                       | 154 ms                                                 | 173 ms: 1.12x slower                                       |
| xml_etree_generate         | 45.8 ms                                                | 51.6 ms: 1.13x slower                                      |
| genshi_text                | 14.4 ms                                                | 16.4 ms: 1.14x slower                                      |
| regex_v8                   | 15.1 ms                                                | 17.3 ms: 1.14x slower                                      |
| scimark_lu                 | 67.7 ms                                                | 78.6 ms: 1.16x slower                                      |
| sqlite_synth               | 1.26 us                                                | 1.57 us: 1.25x slower                                      |
| bench_mp_pool              | 41.0 ms                                                | 51.4 ms: 1.25x slower                                      |
| scimark_sor                | 79.2 ms                                                | 100 ms: 1.27x slower                                       |
| create_gc_cycles           | 711 us                                                 | 903 us: 1.27x slower                                       |
| genshi_xml                 | 28.5 ms                                                | 39.3 ms: 1.38x slower                                      |
| telco                      | 3.17 ms                                                | 4.64 ms: 1.46x slower                                      |
| python_startup             | 10.8 ms                                                | 16.4 ms: 1.52x slower                                      |
| flaskblogging              | 2.35 ms                                                | 3.61 ms: 1.53x slower                                      |
| async_generators           | 192 ms                                                 | 296 ms: 1.54x slower                                       |
| python_startup_no_site     | 8.57 ms                                                | 13.4 ms: 1.57x slower                                      |
| Geometric mean             | (ref)                                                  | 1.01x faster                                               |

Benchmark hidden because not significant (2): tornado_http, pathlib
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
Ignored benchmarks (9) of results/bm-20240605-3.13.0b2-3a83b17-JIT/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, bpe_tokeniser

# HPT report

- Reliability score: 51.10% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.34x