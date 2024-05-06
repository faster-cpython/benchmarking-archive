# Results vs. 3.11.0

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: c179c0e
- commit date: 2024-04-17
- overall geometric mean: 1.11x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 179 ms: 1.16x slower                                   |
| chameleon      | 4.30 ms                                                | 4.81 ms: 1.12x slower                                  |
| docutils       | 1.43 sec                                               | 1.61 sec: 1.12x slower                                 |
| tornado_http   | 69.1 ms                                                | 84.3 ms: 1.22x slower                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_none_tg         | 276 ms                                                 | 208 ms: 1.33x faster                                   |
| async_tree_none            | 282 ms                                                 | 216 ms: 1.30x faster                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 271 ms: 1.30x faster                                   |
| async_tree_io_tg           | 724 ms                                                 | 578 ms: 1.25x faster                                   |
| async_tree_io              | 697 ms                                                 | 586 ms: 1.19x faster                                   |
| async_tree_memoization     | 336 ms                                                 | 284 ms: 1.18x faster                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 475 ms: 1.16x faster                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 476 ms: 1.09x faster                                   |
| Geometric mean             | (ref)                                                  | 1.22x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 284 ms: 1.01x slower                                   |
| float          | 50.8 ms                                                | 75.1 ms: 1.48x slower                                  |
| nbody          | 61.7 ms                                                | 97.8 ms: 1.58x slower                                  |
| Geometric mean | (ref)                                                  | 1.33x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                   |
| regex_effbot   | 2.43 ms                                                | 2.59 ms: 1.06x slower                                  |
| regex_v8       | 15.1 ms                                                | 17.8 ms: 1.18x slower                                  |
| regex_compile  | 72.8 ms                                                | 102 ms: 1.40x slower                                   |
| Geometric mean | (ref)                                                  | 1.15x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.27 ms: 1.20x faster                                  |
| pickle_pure_python   | 191 us                                                 | 186 us: 1.03x faster                                   |
| xml_etree_parse      | 100 ms                                                 | 106 ms: 1.06x slower                                   |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.07x slower                                  |
| pickle               | 6.98 us                                                | 7.51 us: 1.08x slower                                  |
| unpickle_list        | 2.69 us                                                | 2.92 us: 1.09x slower                                  |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                  |
| pickle_list          | 2.70 us                                                | 3.01 us: 1.12x slower                                  |
| unpickle             | 8.29 us                                                | 9.29 us: 1.12x slower                                  |
| xml_etree_iterparse  | 68.3 ms                                                | 80.9 ms: 1.18x slower                                  |
| xml_etree_process    | 33.6 ms                                                | 40.7 ms: 1.21x slower                                  |
| xml_etree_generate   | 45.8 ms                                                | 59.4 ms: 1.30x slower                                  |
| unpickle_pure_python | 149 us                                                 | 202 us: 1.36x slower                                   |
| tomli_loads          | 1.27 sec                                               | 1.83 sec: 1.43x slower                                 |
| Geometric mean       | (ref)                                                  | 1.13x slower                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 8.57 ms                                                | 9.25 ms: 1.08x slower                                  |
| python_startup         | 10.8 ms                                                | 12.1 ms: 1.12x slower                                  |
| Geometric mean         | (ref)                                                  | 1.10x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text     | 14.4 ms                                                | 15.4 ms: 1.07x slower                                  |
| django_template | 20.1 ms                                                | 23.2 ms: 1.15x slower                                  |
| genshi_xml      | 28.5 ms                                                | 33.6 ms: 1.18x slower                                  |
| mako            | 7.93 ms                                                | 10.5 ms: 1.33x slower                                  |
| Geometric mean  | (ref)                                                  | 1.18x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 73.5 us: 4.09x faster                                  |
| asyncio_tcp                | 643 ms                                                 | 415 ms: 1.55x faster                                   |
| pylint                     | 253 ms                                                 | 185 ms: 1.37x faster                                   |
| async_tree_none_tg         | 276 ms                                                 | 208 ms: 1.33x faster                                   |
| async_tree_none            | 282 ms                                                 | 216 ms: 1.30x faster                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 271 ms: 1.30x faster                                   |
| async_tree_io_tg           | 724 ms                                                 | 578 ms: 1.25x faster                                   |
| json_dumps                 | 7.53 ms                                                | 6.27 ms: 1.20x faster                                  |
| async_tree_io              | 697 ms                                                 | 586 ms: 1.19x faster                                   |
| async_tree_memoization     | 336 ms                                                 | 284 ms: 1.18x faster                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 475 ms: 1.16x faster                                   |
| generators                 | 30.3 ms                                                | 27.2 ms: 1.11x faster                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 476 ms: 1.09x faster                                   |
| raytrace                   | 206 ms                                                 | 192 ms: 1.07x faster                                   |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.32 sec: 1.05x faster                                 |
| logging_simple             | 3.41 us                                                | 3.29 us: 1.04x faster                                  |
| pickle_pure_python         | 191 us                                                 | 186 us: 1.03x faster                                   |
| logging_format             | 3.67 us                                                | 3.57 us: 1.03x faster                                  |
| sqlglot_parse              | 890 us                                                 | 868 us: 1.02x faster                                   |
| sqlglot_transpile          | 1.05 ms                                                | 1.04 ms: 1.01x faster                                  |
| coroutines                 | 17.2 ms                                                | 17.0 ms: 1.01x faster                                  |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                   |
| pidigits                   | 280 ms                                                 | 284 ms: 1.01x slower                                   |
| dask                       | 219 ms                                                 | 224 ms: 1.02x slower                                   |
| gc_traversal               | 2.38 ms                                                | 2.45 ms: 1.03x slower                                  |
| dulwich_log                | 28.6 ms                                                | 29.5 ms: 1.03x slower                                  |
| deepcopy                   | 215 us                                                 | 224 us: 1.04x slower                                   |
| pathlib                    | 23.2 ms                                                | 24.4 ms: 1.05x slower                                  |
| pycparser                  | 659 ms                                                 | 693 ms: 1.05x slower                                   |
| sympy_sum                  | 80.2 ms                                                | 84.7 ms: 1.06x slower                                  |
| xml_etree_parse            | 100 ms                                                 | 106 ms: 1.06x slower                                   |
| coverage                   | 43.9 ms                                                | 46.6 ms: 1.06x slower                                  |
| regex_effbot               | 2.43 ms                                                | 2.59 ms: 1.06x slower                                  |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.07x slower                                  |
| genshi_text                | 14.4 ms                                                | 15.4 ms: 1.07x slower                                  |
| bench_mp_pool              | 41.0 ms                                                | 43.7 ms: 1.07x slower                                  |
| json                       | 2.75 ms                                                | 2.94 ms: 1.07x slower                                  |
| pickle                     | 6.98 us                                                | 7.51 us: 1.08x slower                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.93 us: 1.08x slower                                  |
| python_startup_no_site     | 8.57 ms                                                | 9.25 ms: 1.08x slower                                  |
| thrift                     | 410 us                                                 | 446 us: 1.09x slower                                   |
| unpickle_list              | 2.69 us                                                | 2.92 us: 1.09x slower                                  |
| chaos                      | 47.4 ms                                                | 51.8 ms: 1.09x slower                                  |
| gunicorn                   | 1.10 ms                                                | 1.20 ms: 1.10x slower                                  |
| sympy_expand               | 229 ms                                                 | 251 ms: 1.10x slower                                   |
| sympy_integrate            | 11.3 ms                                                | 12.4 ms: 1.10x slower                                  |
| deltablue                  | 2.75 ms                                                | 3.03 ms: 1.10x slower                                  |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                  |
| sympy_str                  | 144 ms                                                 | 159 ms: 1.10x slower                                   |
| bench_thread_pool          | 465 us                                                 | 517 us: 1.11x slower                                   |
| pickle_list                | 2.70 us                                                | 3.01 us: 1.12x slower                                  |
| deepcopy_memo              | 25.7 us                                                | 28.7 us: 1.12x slower                                  |
| unpickle                   | 8.29 us                                                | 9.29 us: 1.12x slower                                  |
| chameleon                  | 4.30 ms                                                | 4.81 ms: 1.12x slower                                  |
| python_startup             | 10.8 ms                                                | 12.1 ms: 1.12x slower                                  |
| aiohttp                    | 1.02 ms                                                | 1.15 ms: 1.12x slower                                  |
| mdp                        | 1.48 sec                                               | 1.67 sec: 1.12x slower                                 |
| mypy2                      | 372 ms                                                 | 418 ms: 1.12x slower                                   |
| docutils                   | 1.43 sec                                               | 1.61 sec: 1.12x slower                                 |
| django_template            | 20.1 ms                                                | 23.2 ms: 1.15x slower                                  |
| 2to3                       | 154 ms                                                 | 179 ms: 1.16x slower                                   |
| sqlglot_normalize          | 162 ms                                                 | 188 ms: 1.16x slower                                   |
| richards_super             | 37.3 ms                                                | 43.6 ms: 1.17x slower                                  |
| regex_v8                   | 15.1 ms                                                | 17.8 ms: 1.18x slower                                  |
| genshi_xml                 | 28.5 ms                                                | 33.6 ms: 1.18x slower                                  |
| xml_etree_iterparse        | 68.3 ms                                                | 80.9 ms: 1.18x slower                                  |
| meteor_contest             | 71.1 ms                                                | 84.9 ms: 1.19x slower                                  |
| xml_etree_process          | 33.6 ms                                                | 40.7 ms: 1.21x slower                                  |
| tornado_http               | 69.1 ms                                                | 84.3 ms: 1.22x slower                                  |
| go                         | 105 ms                                                 | 129 ms: 1.22x slower                                   |
| create_gc_cycles           | 711 us                                                 | 870 us: 1.22x slower                                   |
| sqlglot_optimize           | 29.6 ms                                                | 36.8 ms: 1.24x slower                                  |
| richards                   | 31.1 ms                                                | 40.2 ms: 1.30x slower                                  |
| xml_etree_generate         | 45.8 ms                                                | 59.4 ms: 1.30x slower                                  |
| crypto_pyaes               | 47.5 ms                                                | 62.8 ms: 1.32x slower                                  |
| mako                       | 7.93 ms                                                | 10.5 ms: 1.33x slower                                  |
| sqlite_synth               | 1.26 us                                                | 1.67 us: 1.33x slower                                  |
| comprehensions             | 14.4 us                                                | 19.3 us: 1.34x slower                                  |
| pprint_safe_repr           | 478 ms                                                 | 645 ms: 1.35x slower                                   |
| pprint_pformat             | 979 ms                                                 | 1.33 sec: 1.36x slower                                 |
| unpickle_pure_python       | 149 us                                                 | 202 us: 1.36x slower                                   |
| regex_compile              | 72.8 ms                                                | 102 ms: 1.40x slower                                   |
| nqueens                    | 55.9 ms                                                | 80.0 ms: 1.43x slower                                  |
| tomli_loads                | 1.27 sec                                               | 1.83 sec: 1.43x slower                                 |
| float                      | 50.8 ms                                                | 75.1 ms: 1.48x slower                                  |
| scimark_sor                | 79.2 ms                                                | 117 ms: 1.48x slower                                   |
| hexiom                     | 4.58 ms                                                | 7.01 ms: 1.53x slower                                  |
| telco                      | 3.17 ms                                                | 4.94 ms: 1.56x slower                                  |
| nbody                      | 61.7 ms                                                | 97.8 ms: 1.58x slower                                  |
| fannkuch                   | 240 ms                                                 | 381 ms: 1.59x slower                                   |
| async_generators           | 192 ms                                                 | 306 ms: 1.59x slower                                   |
| scimark_fft                | 173 ms                                                 | 275 ms: 1.59x slower                                   |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 4.60 ms: 1.63x slower                                  |
| scimark_lu                 | 67.7 ms                                                | 111 ms: 1.64x slower                                   |
| scimark_monte_carlo        | 43.5 ms                                                | 71.6 ms: 1.65x slower                                  |
| pyflate                    | 284 ms                                                 | 472 ms: 1.66x slower                                   |
| spectral_norm              | 65.7 ms                                                | 116 ms: 1.77x slower                                   |
| Geometric mean             | (ref)                                                  | 1.11x slower                                           |

Benchmark hidden because not significant (3): asyncio_websockets, html5lib, logging_silent
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240417-3.13.0a6+-c179c0e-PYTHON_UOPS/bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.08x