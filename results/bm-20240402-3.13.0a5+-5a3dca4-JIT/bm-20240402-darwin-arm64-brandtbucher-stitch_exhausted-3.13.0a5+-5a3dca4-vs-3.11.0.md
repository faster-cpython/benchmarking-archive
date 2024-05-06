# Results vs. 3.11.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: darwin-arm64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.02x slower
- HPT reliability: 99.41%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 176 ms: 1.14x slower                                                     |
| chameleon      | 4.30 ms                                                | 4.47 ms: 1.04x slower                                                    |
| docutils       | 1.43 sec                                               | 1.58 sec: 1.11x slower                                                   |
| html5lib       | 33.0 ms                                                | 33.8 ms: 1.02x slower                                                    |
| tornado_http   | 69.1 ms                                                | 82.2 ms: 1.19x slower                                                    |
| Geometric mean | (ref)                                                  | 1.10x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 249 ms: 1.41x faster                                                     |
| async_tree_none_tg         | 276 ms                                                 | 201 ms: 1.38x faster                                                     |
| async_tree_io_tg           | 724 ms                                                 | 557 ms: 1.30x faster                                                     |
| async_tree_memoization     | 336 ms                                                 | 266 ms: 1.26x faster                                                     |
| async_tree_none            | 282 ms                                                 | 228 ms: 1.24x faster                                                     |
| async_tree_io              | 697 ms                                                 | 569 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 462 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 466 ms: 1.11x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 49.2 ms: 1.03x faster                                                    |
| pidigits       | 280 ms                                                 | 283 ms: 1.01x slower                                                     |
| nbody          | 61.7 ms                                                | 70.0 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                  | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 152 ms: 1.03x slower                                                     |
| regex_effbot   | 2.43 ms                                                | 2.62 ms: 1.08x slower                                                    |
| regex_v8       | 15.1 ms                                                | 17.1 ms: 1.13x slower                                                    |
| regex_compile  | 72.8 ms                                                | 87.2 ms: 1.20x slower                                                    |
| Geometric mean | (ref)                                                  | 1.11x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.28 ms: 1.20x faster                                                    |
| pickle_pure_python   | 191 us                                                 | 183 us: 1.05x faster                                                     |
| unpickle_pure_python | 149 us                                                 | 143 us: 1.04x faster                                                     |
| xml_etree_parse      | 100 ms                                                 | 98.3 ms: 1.02x faster                                                    |
| tomli_loads          | 1.27 sec                                               | 1.29 sec: 1.01x slower                                                   |
| pickle_dict          | 17.1 us                                                | 18.0 us: 1.06x slower                                                    |
| pickle               | 6.98 us                                                | 7.47 us: 1.07x slower                                                    |
| xml_etree_process    | 33.6 ms                                                | 36.5 ms: 1.09x slower                                                    |
| pickle_list          | 2.70 us                                                | 2.98 us: 1.10x slower                                                    |
| unpickle             | 8.29 us                                                | 9.17 us: 1.11x slower                                                    |
| json_loads           | 15.3 us                                                | 17.1 us: 1.11x slower                                                    |
| unpickle_list        | 2.69 us                                                | 3.04 us: 1.13x slower                                                    |
| xml_etree_generate   | 45.8 ms                                                | 54.1 ms: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 13.4 ms: 1.24x slower                                                    |
| python_startup_no_site | 8.57 ms                                                | 11.6 ms: 1.35x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.30x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.96 ms: 1.14x faster                                                    |
| genshi_text     | 14.4 ms                                                | 14.7 ms: 1.02x slower                                                    |
| django_template | 20.1 ms                                                | 21.3 ms: 1.06x slower                                                    |
| genshi_xml      | 28.5 ms                                                | 32.7 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 69.9 us: 4.31x faster                                                    |
| pylint                     | 253 ms                                                 | 159 ms: 1.59x faster                                                     |
| asyncio_tcp                | 643 ms                                                 | 449 ms: 1.43x faster                                                     |
| async_tree_memoization_tg  | 352 ms                                                 | 249 ms: 1.41x faster                                                     |
| async_tree_none_tg         | 276 ms                                                 | 201 ms: 1.38x faster                                                     |
| async_tree_io_tg           | 724 ms                                                 | 557 ms: 1.30x faster                                                     |
| async_tree_memoization     | 336 ms                                                 | 266 ms: 1.26x faster                                                     |
| async_tree_none            | 282 ms                                                 | 228 ms: 1.24x faster                                                     |
| async_tree_io              | 697 ms                                                 | 569 ms: 1.22x faster                                                     |
| chaos                      | 47.4 ms                                                | 39.4 ms: 1.20x faster                                                    |
| json_dumps                 | 7.53 ms                                                | 6.28 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 462 ms: 1.19x faster                                                     |
| comprehensions             | 14.4 us                                                | 12.1 us: 1.19x faster                                                    |
| deltablue                  | 2.75 ms                                                | 2.37 ms: 1.16x faster                                                    |
| sqlglot_parse              | 890 us                                                 | 769 us: 1.16x faster                                                     |
| generators                 | 30.3 ms                                                | 26.2 ms: 1.16x faster                                                    |
| mako                       | 7.93 ms                                                | 6.96 ms: 1.14x faster                                                    |
| raytrace                   | 206 ms                                                 | 181 ms: 1.13x faster                                                     |
| sqlglot_transpile          | 1.05 ms                                                | 944 us: 1.11x faster                                                     |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 466 ms: 1.11x faster                                                     |
| richards_super             | 37.3 ms                                                | 34.8 ms: 1.07x faster                                                    |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.30 sec: 1.07x faster                                                   |
| deepcopy_memo              | 25.7 us                                                | 24.3 us: 1.06x faster                                                    |
| pickle_pure_python         | 191 us                                                 | 183 us: 1.05x faster                                                     |
| unpickle_pure_python       | 149 us                                                 | 143 us: 1.04x faster                                                     |
| logging_simple             | 3.41 us                                                | 3.29 us: 1.04x faster                                                    |
| float                      | 50.8 ms                                                | 49.2 ms: 1.03x faster                                                    |
| sympy_sum                  | 80.2 ms                                                | 77.9 ms: 1.03x faster                                                    |
| coroutines                 | 17.2 ms                                                | 16.7 ms: 1.03x faster                                                    |
| logging_format             | 3.67 us                                                | 3.59 us: 1.02x faster                                                    |
| xml_etree_parse            | 100 ms                                                 | 98.3 ms: 1.02x faster                                                    |
| logging_silent             | 66.5 ns                                                | 65.7 ns: 1.01x faster                                                    |
| sympy_str                  | 144 ms                                                 | 143 ms: 1.01x faster                                                     |
| richards                   | 31.1 ms                                                | 31.2 ms: 1.00x slower                                                    |
| pidigits                   | 280 ms                                                 | 283 ms: 1.01x slower                                                     |
| tomli_loads                | 1.27 sec                                               | 1.29 sec: 1.01x slower                                                   |
| go                         | 105 ms                                                 | 107 ms: 1.02x slower                                                     |
| genshi_text                | 14.4 ms                                                | 14.7 ms: 1.02x slower                                                    |
| html5lib                   | 33.0 ms                                                | 33.8 ms: 1.02x slower                                                    |
| gc_traversal               | 2.38 ms                                                | 2.45 ms: 1.03x slower                                                    |
| regex_dna                  | 148 ms                                                 | 152 ms: 1.03x slower                                                     |
| dask                       | 219 ms                                                 | 226 ms: 1.03x slower                                                     |
| sympy_integrate            | 11.3 ms                                                | 11.7 ms: 1.04x slower                                                    |
| chameleon                  | 4.30 ms                                                | 4.47 ms: 1.04x slower                                                    |
| deepcopy_reduce            | 1.79 us                                                | 1.87 us: 1.04x slower                                                    |
| meteor_contest             | 71.1 ms                                                | 74.4 ms: 1.05x slower                                                    |
| sympy_expand               | 229 ms                                                 | 241 ms: 1.05x slower                                                     |
| scimark_monte_carlo        | 43.5 ms                                                | 45.9 ms: 1.06x slower                                                    |
| pickle_dict                | 17.1 us                                                | 18.0 us: 1.06x slower                                                    |
| dulwich_log                | 28.6 ms                                                | 30.2 ms: 1.06x slower                                                    |
| coverage                   | 43.9 ms                                                | 46.4 ms: 1.06x slower                                                    |
| django_template            | 20.1 ms                                                | 21.3 ms: 1.06x slower                                                    |
| mdp                        | 1.48 sec                                               | 1.58 sec: 1.06x slower                                                   |
| pathlib                    | 23.2 ms                                                | 24.7 ms: 1.07x slower                                                    |
| thrift                     | 410 us                                                 | 437 us: 1.07x slower                                                     |
| pickle                     | 6.98 us                                                | 7.47 us: 1.07x slower                                                    |
| json                       | 2.75 ms                                                | 2.95 ms: 1.07x slower                                                    |
| fannkuch                   | 240 ms                                                 | 258 ms: 1.08x slower                                                     |
| bench_thread_pool          | 465 us                                                 | 501 us: 1.08x slower                                                     |
| regex_effbot               | 2.43 ms                                                | 2.62 ms: 1.08x slower                                                    |
| xml_etree_process          | 33.6 ms                                                | 36.5 ms: 1.09x slower                                                    |
| pprint_pformat             | 979 ms                                                 | 1.07 sec: 1.09x slower                                                   |
| sqlglot_normalize          | 162 ms                                                 | 178 ms: 1.10x slower                                                     |
| nqueens                    | 55.9 ms                                                | 61.6 ms: 1.10x slower                                                    |
| pprint_safe_repr           | 478 ms                                                 | 527 ms: 1.10x slower                                                     |
| gunicorn                   | 1.10 ms                                                | 1.21 ms: 1.10x slower                                                    |
| pickle_list                | 2.70 us                                                | 2.98 us: 1.10x slower                                                    |
| unpickle                   | 8.29 us                                                | 9.17 us: 1.11x slower                                                    |
| docutils                   | 1.43 sec                                               | 1.58 sec: 1.11x slower                                                   |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.13 ms: 1.11x slower                                                    |
| json_loads                 | 15.3 us                                                | 17.1 us: 1.11x slower                                                    |
| aiohttp                    | 1.02 ms                                                | 1.14 ms: 1.11x slower                                                    |
| spectral_norm              | 65.7 ms                                                | 73.8 ms: 1.12x slower                                                    |
| regex_v8                   | 15.1 ms                                                | 17.1 ms: 1.13x slower                                                    |
| unpickle_list              | 2.69 us                                                | 3.04 us: 1.13x slower                                                    |
| nbody                      | 61.7 ms                                                | 70.0 ms: 1.13x slower                                                    |
| 2to3                       | 154 ms                                                 | 176 ms: 1.14x slower                                                     |
| mypy2                      | 372 ms                                                 | 426 ms: 1.14x slower                                                     |
| genshi_xml                 | 28.5 ms                                                | 32.7 ms: 1.14x slower                                                    |
| bench_mp_pool              | 41.0 ms                                                | 47.0 ms: 1.15x slower                                                    |
| hexiom                     | 4.58 ms                                                | 5.28 ms: 1.15x slower                                                    |
| scimark_fft                | 173 ms                                                 | 200 ms: 1.16x slower                                                     |
| sqlglot_optimize           | 29.6 ms                                                | 34.4 ms: 1.16x slower                                                    |
| pyflate                    | 284 ms                                                 | 335 ms: 1.18x slower                                                     |
| xml_etree_generate         | 45.8 ms                                                | 54.1 ms: 1.18x slower                                                    |
| tornado_http               | 69.1 ms                                                | 82.2 ms: 1.19x slower                                                    |
| create_gc_cycles           | 711 us                                                 | 847 us: 1.19x slower                                                     |
| regex_compile              | 72.8 ms                                                | 87.2 ms: 1.20x slower                                                    |
| scimark_lu                 | 67.7 ms                                                | 81.5 ms: 1.20x slower                                                    |
| python_startup             | 10.8 ms                                                | 13.4 ms: 1.24x slower                                                    |
| sqlite_synth               | 1.26 us                                                | 1.58 us: 1.26x slower                                                    |
| python_startup_no_site     | 8.57 ms                                                | 11.6 ms: 1.35x slower                                                    |
| scimark_sor                | 79.2 ms                                                | 108 ms: 1.36x slower                                                     |
| telco                      | 3.17 ms                                                | 4.48 ms: 1.41x slower                                                    |
| async_generators           | 192 ms                                                 | 301 ms: 1.57x slower                                                     |
| unpack_sequence            | 33.6 ns                                                | 116 ns: 3.45x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                             |

Benchmark hidden because not significant (5): deepcopy, crypto_pyaes, asyncio_websockets, xml_etree_iterparse, pycparser
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (8) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 99.41% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.33x