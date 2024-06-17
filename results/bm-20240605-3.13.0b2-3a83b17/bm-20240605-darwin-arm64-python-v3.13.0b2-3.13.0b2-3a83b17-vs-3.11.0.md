# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b2
- machine: darwin-arm64
- commit hash: 3a83b17
- commit date: 2024-06-05
- overall geometric mean: 1.04x faster
- HPT reliability: 93.86%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 161 ms: 1.04x slower                                       |
| chameleon      | 4.30 ms                                                | 4.27 ms: 1.01x faster                                      |
| docutils       | 1.43 sec                                               | 1.44 sec: 1.01x slower                                     |
| html5lib       | 33.0 ms                                                | 31.2 ms: 1.06x faster                                      |
| Geometric mean | (ref)                                                  | 1.01x faster                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 240 ms: 1.47x faster                                       |
| async_tree_none_tg         | 276 ms                                                 | 198 ms: 1.40x faster                                       |
| async_tree_none            | 282 ms                                                 | 209 ms: 1.35x faster                                       |
| async_tree_memoization     | 336 ms                                                 | 260 ms: 1.29x faster                                       |
| async_tree_io_tg           | 724 ms                                                 | 565 ms: 1.28x faster                                       |
| async_tree_io              | 697 ms                                                 | 563 ms: 1.24x faster                                       |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 451 ms: 1.22x faster                                       |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 467 ms: 1.11x faster                                       |
| Geometric mean             | (ref)                                                  | 1.29x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 50.8 ms                                                | 48.6 ms: 1.05x faster                                      |
| nbody          | 61.7 ms                                                | 59.6 ms: 1.04x faster                                      |
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                       |
| Geometric mean | (ref)                                                  | 1.02x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 68.5 ms: 1.06x faster                                      |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                       |
| regex_effbot   | 2.43 ms                                                | 2.58 ms: 1.06x slower                                      |
| regex_v8       | 15.1 ms                                                | 17.3 ms: 1.14x slower                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.23 ms: 1.21x faster                                      |
| pickle_pure_python   | 191 us                                                 | 179 us: 1.07x faster                                       |
| unpickle_pure_python | 149 us                                                 | 141 us: 1.06x faster                                       |
| xml_etree_iterparse  | 68.3 ms                                                | 71.5 ms: 1.05x slower                                      |
| xml_etree_parse      | 100 ms                                                 | 106 ms: 1.05x slower                                       |
| pickle_dict          | 17.1 us                                                | 18.3 us: 1.07x slower                                      |
| pickle               | 6.98 us                                                | 7.48 us: 1.07x slower                                      |
| unpickle_list        | 2.69 us                                                | 2.88 us: 1.07x slower                                      |
| pickle_list          | 2.70 us                                                | 2.96 us: 1.10x slower                                      |
| json_loads           | 15.3 us                                                | 16.8 us: 1.10x slower                                      |
| unpickle             | 8.29 us                                                | 9.12 us: 1.10x slower                                      |
| xml_etree_process    | 33.6 ms                                                | 37.1 ms: 1.10x slower                                      |
| xml_etree_generate   | 45.8 ms                                                | 52.7 ms: 1.15x slower                                      |
| tomli_loads          | 1.27 sec                                               | 1.47 sec: 1.15x slower                                     |
| Geometric mean       | (ref)                                                  | 1.05x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 15.2 ms: 1.41x slower                                      |
| python_startup_no_site | 8.57 ms                                                | 12.3 ms: 1.44x slower                                      |
| Geometric mean         | (ref)                                                  | 1.42x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.99 ms: 1.14x faster                                      |
| django_template | 20.1 ms                                                | 19.4 ms: 1.04x faster                                      |
| genshi_text     | 14.4 ms                                                | 13.9 ms: 1.04x faster                                      |
| genshi_xml      | 28.5 ms                                                | 29.9 ms: 1.05x slower                                      |
| Geometric mean  | (ref)                                                  | 1.04x faster                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 87.6 us: 3.44x faster                                      |
| asyncio_tcp                | 643 ms                                                 | 402 ms: 1.60x faster                                       |
| pylint                     | 253 ms                                                 | 170 ms: 1.49x faster                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 240 ms: 1.47x faster                                       |
| comprehensions             | 14.4 us                                                | 10.2 us: 1.42x faster                                      |
| raytrace                   | 206 ms                                                 | 147 ms: 1.40x faster                                       |
| async_tree_none_tg         | 276 ms                                                 | 198 ms: 1.40x faster                                       |
| chaos                      | 47.4 ms                                                | 34.0 ms: 1.39x faster                                      |
| async_tree_none            | 282 ms                                                 | 209 ms: 1.35x faster                                       |
| generators                 | 30.3 ms                                                | 22.9 ms: 1.32x faster                                      |
| async_tree_memoization     | 336 ms                                                 | 260 ms: 1.29x faster                                       |
| deltablue                  | 2.75 ms                                                | 2.14 ms: 1.28x faster                                      |
| async_tree_io_tg           | 724 ms                                                 | 565 ms: 1.28x faster                                       |
| async_tree_io              | 697 ms                                                 | 563 ms: 1.24x faster                                       |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 451 ms: 1.22x faster                                       |
| sqlglot_parse              | 890 us                                                 | 732 us: 1.22x faster                                       |
| json_dumps                 | 7.53 ms                                                | 6.23 ms: 1.21x faster                                      |
| sqlglot_transpile          | 1.05 ms                                                | 891 us: 1.18x faster                                       |
| sympy_sum                  | 80.2 ms                                                | 69.2 ms: 1.16x faster                                      |
| deepcopy_memo              | 25.7 us                                                | 22.6 us: 1.14x faster                                      |
| mako                       | 7.93 ms                                                | 6.99 ms: 1.14x faster                                      |
| hexiom                     | 4.58 ms                                                | 4.06 ms: 1.13x faster                                      |
| logging_simple             | 3.41 us                                                | 3.04 us: 1.12x faster                                      |
| logging_format             | 3.67 us                                                | 3.31 us: 1.11x faster                                      |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 467 ms: 1.11x faster                                       |
| logging_silent             | 66.5 ns                                                | 60.1 ns: 1.11x faster                                      |
| sympy_str                  | 144 ms                                                 | 131 ms: 1.09x faster                                       |
| sympy_integrate            | 11.3 ms                                                | 10.3 ms: 1.09x faster                                      |
| coroutines                 | 17.2 ms                                                | 15.8 ms: 1.08x faster                                      |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.29 sec: 1.08x faster                                     |
| pickle_pure_python         | 191 us                                                 | 179 us: 1.07x faster                                       |
| nqueens                    | 55.9 ms                                                | 52.2 ms: 1.07x faster                                      |
| regex_compile              | 72.8 ms                                                | 68.5 ms: 1.06x faster                                      |
| richards_super             | 37.3 ms                                                | 35.2 ms: 1.06x faster                                      |
| html5lib                   | 33.0 ms                                                | 31.2 ms: 1.06x faster                                      |
| gunicorn                   | 1.10 ms                                                | 1.04 ms: 1.06x faster                                      |
| unpickle_pure_python       | 149 us                                                 | 141 us: 1.06x faster                                       |
| deepcopy                   | 215 us                                                 | 204 us: 1.06x faster                                       |
| go                         | 105 ms                                                 | 101 ms: 1.05x faster                                       |
| float                      | 50.8 ms                                                | 48.6 ms: 1.05x faster                                      |
| pycparser                  | 659 ms                                                 | 632 ms: 1.04x faster                                       |
| bench_thread_pool          | 465 us                                                 | 447 us: 1.04x faster                                       |
| dulwich_log                | 28.6 ms                                                | 27.6 ms: 1.04x faster                                      |
| django_template            | 20.1 ms                                                | 19.4 ms: 1.04x faster                                      |
| genshi_text                | 14.4 ms                                                | 13.9 ms: 1.04x faster                                      |
| nbody                      | 61.7 ms                                                | 59.6 ms: 1.04x faster                                      |
| pprint_pformat             | 979 ms                                                 | 947 ms: 1.03x faster                                       |
| pprint_safe_repr           | 478 ms                                                 | 465 ms: 1.03x faster                                       |
| aiohttp                    | 1.02 ms                                                | 997 us: 1.03x faster                                       |
| scimark_monte_carlo        | 43.5 ms                                                | 42.5 ms: 1.02x faster                                      |
| sympy_expand               | 229 ms                                                 | 226 ms: 1.01x faster                                       |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.77 ms: 1.01x faster                                      |
| scimark_lu                 | 67.7 ms                                                | 66.9 ms: 1.01x faster                                      |
| meteor_contest             | 71.1 ms                                                | 70.3 ms: 1.01x faster                                      |
| chameleon                  | 4.30 ms                                                | 4.27 ms: 1.01x faster                                      |
| asyncio_websockets         | 408 ms                                                 | 409 ms: 1.00x slower                                       |
| docutils                   | 1.43 sec                                               | 1.44 sec: 1.01x slower                                     |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                       |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                       |
| spectral_norm              | 65.7 ms                                                | 66.4 ms: 1.01x slower                                      |
| deepcopy_reduce            | 1.79 us                                                | 1.82 us: 1.02x slower                                      |
| mypy2                      | 372 ms                                                 | 379 ms: 1.02x slower                                       |
| sqlglot_normalize          | 162 ms                                                 | 166 ms: 1.02x slower                                       |
| richards                   | 31.1 ms                                                | 31.8 ms: 1.03x slower                                      |
| coverage                   | 43.9 ms                                                | 45.0 ms: 1.03x slower                                      |
| gc_traversal               | 2.38 ms                                                | 2.45 ms: 1.03x slower                                      |
| mdp                        | 1.48 sec                                               | 1.53 sec: 1.03x slower                                     |
| fannkuch                   | 240 ms                                                 | 248 ms: 1.04x slower                                       |
| crypto_pyaes               | 47.5 ms                                                | 49.5 ms: 1.04x slower                                      |
| sqlglot_optimize           | 29.6 ms                                                | 30.9 ms: 1.04x slower                                      |
| 2to3                       | 154 ms                                                 | 161 ms: 1.04x slower                                       |
| scimark_fft                | 173 ms                                                 | 181 ms: 1.05x slower                                       |
| xml_etree_iterparse        | 68.3 ms                                                | 71.5 ms: 1.05x slower                                      |
| genshi_xml                 | 28.5 ms                                                | 29.9 ms: 1.05x slower                                      |
| xml_etree_parse            | 100 ms                                                 | 106 ms: 1.05x slower                                       |
| thrift                     | 410 us                                                 | 435 us: 1.06x slower                                       |
| regex_effbot               | 2.43 ms                                                | 2.58 ms: 1.06x slower                                      |
| json                       | 2.75 ms                                                | 2.93 ms: 1.06x slower                                      |
| pickle_dict                | 17.1 us                                                | 18.3 us: 1.07x slower                                      |
| pickle                     | 6.98 us                                                | 7.48 us: 1.07x slower                                      |
| unpickle_list              | 2.69 us                                                | 2.88 us: 1.07x slower                                      |
| pickle_list                | 2.70 us                                                | 2.96 us: 1.10x slower                                      |
| json_loads                 | 15.3 us                                                | 16.8 us: 1.10x slower                                      |
| unpickle                   | 8.29 us                                                | 9.12 us: 1.10x slower                                      |
| xml_etree_process          | 33.6 ms                                                | 37.1 ms: 1.10x slower                                      |
| pyflate                    | 284 ms                                                 | 321 ms: 1.13x slower                                       |
| regex_v8                   | 15.1 ms                                                | 17.3 ms: 1.14x slower                                      |
| xml_etree_generate         | 45.8 ms                                                | 52.7 ms: 1.15x slower                                      |
| tomli_loads                | 1.27 sec                                               | 1.47 sec: 1.15x slower                                     |
| bench_mp_pool              | 41.0 ms                                                | 47.2 ms: 1.15x slower                                      |
| scimark_sor                | 79.2 ms                                                | 94.9 ms: 1.20x slower                                      |
| sqlite_synth               | 1.26 us                                                | 1.55 us: 1.24x slower                                      |
| create_gc_cycles           | 711 us                                                 | 897 us: 1.26x slower                                       |
| python_startup             | 10.8 ms                                                | 15.2 ms: 1.41x slower                                      |
| python_startup_no_site     | 8.57 ms                                                | 12.3 ms: 1.44x slower                                      |
| telco                      | 3.17 ms                                                | 4.60 ms: 1.45x slower                                      |
| async_generators           | 192 ms                                                 | 281 ms: 1.46x slower                                       |
| flaskblogging              | 2.35 ms                                                | 3.61 ms: 1.53x slower                                      |
| Geometric mean             | (ref)                                                  | 1.04x faster                                               |

Benchmark hidden because not significant (3): tornado_http, pathlib, dask
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (9) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, bpe_tokeniser

# HPT report

- Reliability score: 93.86% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x