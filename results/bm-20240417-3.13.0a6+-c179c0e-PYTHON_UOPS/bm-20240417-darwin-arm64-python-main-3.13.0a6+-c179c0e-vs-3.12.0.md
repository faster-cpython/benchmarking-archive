# Results vs. 3.12.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: c179c0e
- commit date: 2024-04-17
- overall geometric mean: 1.08x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 179 ms: 1.05x slower                                   |
| chameleon      | 4.70 ms                                                | 4.81 ms: 1.03x slower                                  |
| docutils       | 1.50 sec                                               | 1.61 sec: 1.07x slower                                 |
| tornado_http   | 69.3 ms                                                | 84.3 ms: 1.22x slower                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_none_tg         | 258 ms                                                 | 208 ms: 1.24x faster                                   |
| async_tree_none            | 266 ms                                                 | 216 ms: 1.23x faster                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 271 ms: 1.19x faster                                   |
| async_tree_io_tg           | 669 ms                                                 | 578 ms: 1.16x faster                                   |
| async_tree_io              | 668 ms                                                 | 586 ms: 1.14x faster                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 475 ms: 1.12x faster                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 476 ms: 1.10x faster                                   |
| async_tree_memoization     | 312 ms                                                 | 284 ms: 1.10x faster                                   |
| Geometric mean             | (ref)                                                  | 1.16x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 282 ms                                                 | 284 ms: 1.01x slower                                   |
| float          | 55.8 ms                                                | 75.1 ms: 1.35x slower                                  |
| nbody          | 68.8 ms                                                | 97.8 ms: 1.42x slower                                  |
| Geometric mean | (ref)                                                  | 1.24x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_dna      | 154 ms                                                 | 149 ms: 1.03x faster                                   |
| regex_effbot   | 2.64 ms                                                | 2.59 ms: 1.02x faster                                  |
| regex_v8       | 16.0 ms                                                | 17.8 ms: 1.12x slower                                  |
| regex_compile  | 77.9 ms                                                | 102 ms: 1.31x slower                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 186 us: 1.08x faster                                   |
| unpickle_list        | 3.02 us                                                | 2.92 us: 1.03x faster                                  |
| json_loads           | 17.2 us                                                | 16.9 us: 1.02x faster                                  |
| json_dumps           | 6.22 ms                                                | 6.27 ms: 1.01x slower                                  |
| pickle_dict          | 18.1 us                                                | 18.2 us: 1.01x slower                                  |
| unpickle             | 9.12 us                                                | 9.29 us: 1.02x slower                                  |
| xml_etree_process    | 39.7 ms                                                | 40.7 ms: 1.03x slower                                  |
| pickle               | 7.23 us                                                | 7.51 us: 1.04x slower                                  |
| pickle_list          | 2.89 us                                                | 3.01 us: 1.04x slower                                  |
| xml_etree_generate   | 55.8 ms                                                | 59.4 ms: 1.06x slower                                  |
| xml_etree_iterparse  | 74.0 ms                                                | 80.9 ms: 1.09x slower                                  |
| tomli_loads          | 1.39 sec                                               | 1.83 sec: 1.31x slower                                 |
| unpickle_pure_python | 151 us                                                 | 202 us: 1.34x slower                                   |
| Geometric mean       | (ref)                                                  | 1.05x slower                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 9.37 ms                                                | 9.25 ms: 1.01x faster                                  |
| python_startup         | 11.4 ms                                                | 12.1 ms: 1.06x slower                                  |
| Geometric mean         | (ref)                                                  | 1.02x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 22.3 ms                                                | 23.2 ms: 1.04x slower                                  |
| mako            | 7.71 ms                                                | 10.5 ms: 1.37x slower                                  |
| Geometric mean  | (ref)                                                  | 1.19x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols   | 93.0 us                                                | 73.5 us: 1.26x faster                                  |
| async_tree_none_tg         | 258 ms                                                 | 208 ms: 1.24x faster                                   |
| async_tree_none            | 266 ms                                                 | 216 ms: 1.23x faster                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 271 ms: 1.19x faster                                   |
| async_tree_io_tg           | 669 ms                                                 | 578 ms: 1.16x faster                                   |
| logging_silent             | 76.4 ns                                                | 66.6 ns: 1.15x faster                                  |
| generators                 | 31.1 ms                                                | 27.2 ms: 1.14x faster                                  |
| async_tree_io              | 668 ms                                                 | 586 ms: 1.14x faster                                   |
| coroutines                 | 19.2 ms                                                | 17.0 ms: 1.13x faster                                  |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 475 ms: 1.12x faster                                   |
| logging_simple             | 3.69 us                                                | 3.29 us: 1.12x faster                                  |
| logging_format             | 3.98 us                                                | 3.57 us: 1.11x faster                                  |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 476 ms: 1.10x faster                                   |
| raytrace                   | 212 ms                                                 | 192 ms: 1.10x faster                                   |
| async_tree_memoization     | 312 ms                                                 | 284 ms: 1.10x faster                                   |
| asyncio_tcp                | 449 ms                                                 | 415 ms: 1.08x faster                                   |
| pickle_pure_python         | 200 us                                                 | 186 us: 1.08x faster                                   |
| deepcopy_reduce            | 2.07 us                                                | 1.93 us: 1.07x faster                                  |
| json                       | 3.09 ms                                                | 2.94 ms: 1.05x faster                                  |
| deepcopy                   | 235 us                                                 | 224 us: 1.05x faster                                   |
| regex_dna                  | 154 ms                                                 | 149 ms: 1.03x faster                                   |
| unpickle_list              | 3.02 us                                                | 2.92 us: 1.03x faster                                  |
| bench_mp_pool              | 44.9 ms                                                | 43.7 ms: 1.03x faster                                  |
| regex_effbot               | 2.64 ms                                                | 2.59 ms: 1.02x faster                                  |
| json_loads                 | 17.2 us                                                | 16.9 us: 1.02x faster                                  |
| python_startup_no_site     | 9.37 ms                                                | 9.25 ms: 1.01x faster                                  |
| dulwich_log                | 29.8 ms                                                | 29.5 ms: 1.01x faster                                  |
| asyncio_websockets         | 409 ms                                                 | 408 ms: 1.00x faster                                   |
| async_generators           | 304 ms                                                 | 306 ms: 1.01x slower                                   |
| pidigits                   | 282 ms                                                 | 284 ms: 1.01x slower                                   |
| json_dumps                 | 6.22 ms                                                | 6.27 ms: 1.01x slower                                  |
| pickle_dict                | 18.1 us                                                | 18.2 us: 1.01x slower                                  |
| sqlglot_normalize          | 186 ms                                                 | 188 ms: 1.01x slower                                   |
| unpickle                   | 9.12 us                                                | 9.29 us: 1.02x slower                                  |
| sqlglot_transpile          | 1.02 ms                                                | 1.04 ms: 1.02x slower                                  |
| gc_traversal               | 2.40 ms                                                | 2.45 ms: 1.02x slower                                  |
| pycparser                  | 677 ms                                                 | 693 ms: 1.02x slower                                   |
| sqlglot_parse              | 848 us                                                 | 868 us: 1.02x slower                                   |
| bench_thread_pool          | 504 us                                                 | 517 us: 1.02x slower                                   |
| chameleon                  | 4.70 ms                                                | 4.81 ms: 1.03x slower                                  |
| xml_etree_process          | 39.7 ms                                                | 40.7 ms: 1.03x slower                                  |
| deepcopy_memo              | 27.7 us                                                | 28.7 us: 1.04x slower                                  |
| pickle                     | 7.23 us                                                | 7.51 us: 1.04x slower                                  |
| django_template            | 22.3 ms                                                | 23.2 ms: 1.04x slower                                  |
| pickle_list                | 2.89 us                                                | 3.01 us: 1.04x slower                                  |
| sympy_expand               | 241 ms                                                 | 251 ms: 1.04x slower                                   |
| gunicorn                   | 1.15 ms                                                | 1.20 ms: 1.05x slower                                  |
| mdp                        | 1.58 sec                                               | 1.67 sec: 1.05x slower                                 |
| 2to3                       | 169 ms                                                 | 179 ms: 1.05x slower                                   |
| python_startup             | 11.4 ms                                                | 12.1 ms: 1.06x slower                                  |
| sqlite_synth               | 1.57 us                                                | 1.67 us: 1.06x slower                                  |
| xml_etree_generate         | 55.8 ms                                                | 59.4 ms: 1.06x slower                                  |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.32 sec: 1.06x slower                                 |
| aiohttp                    | 1.08 ms                                                | 1.15 ms: 1.06x slower                                  |
| docutils                   | 1.50 sec                                               | 1.61 sec: 1.07x slower                                 |
| sympy_str                  | 148 ms                                                 | 159 ms: 1.08x slower                                   |
| sqlglot_optimize           | 34.0 ms                                                | 36.8 ms: 1.08x slower                                  |
| sympy_sum                  | 77.6 ms                                                | 84.7 ms: 1.09x slower                                  |
| sympy_integrate            | 11.4 ms                                                | 12.4 ms: 1.09x slower                                  |
| xml_etree_iterparse        | 74.0 ms                                                | 80.9 ms: 1.09x slower                                  |
| mypy2                      | 380 ms                                                 | 418 ms: 1.10x slower                                   |
| regex_v8                   | 16.0 ms                                                | 17.8 ms: 1.12x slower                                  |
| deltablue                  | 2.71 ms                                                | 3.03 ms: 1.12x slower                                  |
| meteor_contest             | 71.7 ms                                                | 84.9 ms: 1.18x slower                                  |
| coverage                   | 38.9 ms                                                | 46.6 ms: 1.20x slower                                  |
| richards_super             | 36.0 ms                                                | 43.6 ms: 1.21x slower                                  |
| crypto_pyaes               | 51.9 ms                                                | 62.8 ms: 1.21x slower                                  |
| tornado_http               | 69.3 ms                                                | 84.3 ms: 1.22x slower                                  |
| chaos                      | 42.5 ms                                                | 51.8 ms: 1.22x slower                                  |
| create_gc_cycles           | 701 us                                                 | 870 us: 1.24x slower                                   |
| richards                   | 32.1 ms                                                | 40.2 ms: 1.25x slower                                  |
| go                         | 102 ms                                                 | 129 ms: 1.27x slower                                   |
| nqueens                    | 62.4 ms                                                | 80.0 ms: 1.28x slower                                  |
| pprint_safe_repr           | 497 ms                                                 | 645 ms: 1.30x slower                                   |
| regex_compile              | 77.9 ms                                                | 102 ms: 1.31x slower                                   |
| tomli_loads                | 1.39 sec                                               | 1.83 sec: 1.31x slower                                 |
| pprint_pformat             | 1.01 sec                                               | 1.33 sec: 1.31x slower                                 |
| comprehensions             | 14.5 us                                                | 19.3 us: 1.33x slower                                  |
| unpickle_pure_python       | 151 us                                                 | 202 us: 1.34x slower                                   |
| scimark_sor                | 87.4 ms                                                | 117 ms: 1.34x slower                                   |
| telco                      | 3.68 ms                                                | 4.94 ms: 1.34x slower                                  |
| float                      | 55.8 ms                                                | 75.1 ms: 1.35x slower                                  |
| mako                       | 7.71 ms                                                | 10.5 ms: 1.37x slower                                  |
| scimark_fft                | 195 ms                                                 | 275 ms: 1.41x slower                                   |
| nbody                      | 68.8 ms                                                | 97.8 ms: 1.42x slower                                  |
| scimark_lu                 | 76.0 ms                                                | 111 ms: 1.46x slower                                   |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 4.60 ms: 1.47x slower                                  |
| pyflate                    | 316 ms                                                 | 472 ms: 1.49x slower                                   |
| spectral_norm              | 76.4 ms                                                | 116 ms: 1.52x slower                                   |
| fannkuch                   | 248 ms                                                 | 381 ms: 1.53x slower                                   |
| hexiom                     | 4.54 ms                                                | 7.01 ms: 1.54x slower                                  |
| scimark_monte_carlo        | 45.0 ms                                                | 71.6 ms: 1.59x slower                                  |
| Geometric mean             | (ref)                                                  | 1.08x slower                                           |

Benchmark hidden because not significant (3): xml_etree_parse, pathlib, dask
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240417-3.13.0a6+-c179c0e-PYTHON_UOPS/bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.05x