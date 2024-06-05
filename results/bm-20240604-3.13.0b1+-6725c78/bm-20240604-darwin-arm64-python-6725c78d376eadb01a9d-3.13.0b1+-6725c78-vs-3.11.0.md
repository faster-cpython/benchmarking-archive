# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: darwin-arm64
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.04x faster
- HPT reliability: 98.27%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.72x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 161 ms: 1.04x slower                                                   |
| html5lib       | 33.0 ms                                                | 31.4 ms: 1.05x faster                                                  |
| tornado_http   | 69.1 ms                                                | 65.4 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (2): chameleon, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 237 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 195 ms: 1.42x faster                                                   |
| async_tree_none            | 282 ms                                                 | 207 ms: 1.36x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 255 ms: 1.32x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 557 ms: 1.30x faster                                                   |
| async_tree_io              | 697 ms                                                 | 558 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 451 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 465 ms: 1.12x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.30x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 48.7 ms: 1.04x faster                                                  |
| nbody          | 61.7 ms                                                | 60.9 ms: 1.01x faster                                                  |
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 68.5 ms: 1.06x faster                                                  |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.3 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.42 ms: 1.17x faster                                                  |
| pickle_pure_python   | 191 us                                                 | 178 us: 1.08x faster                                                   |
| unpickle_pure_python | 149 us                                                 | 142 us: 1.04x faster                                                   |
| xml_etree_parse      | 100 ms                                                 | 102 ms: 1.02x slower                                                   |
| xml_etree_iterparse  | 68.3 ms                                                | 71.7 ms: 1.05x slower                                                  |
| pickle               | 6.98 us                                                | 7.49 us: 1.07x slower                                                  |
| pickle_dict          | 17.1 us                                                | 18.5 us: 1.08x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.91 us: 1.08x slower                                                  |
| pickle_list          | 2.70 us                                                | 2.99 us: 1.11x slower                                                  |
| unpickle             | 8.29 us                                                | 9.22 us: 1.11x slower                                                  |
| json_loads           | 15.3 us                                                | 17.1 us: 1.11x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 37.3 ms: 1.11x slower                                                  |
| tomli_loads          | 1.27 sec                                               | 1.44 sec: 1.13x slower                                                 |
| xml_etree_generate   | 45.8 ms                                                | 52.3 ms: 1.14x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 8.57 ms                                                | 11.2 ms: 1.31x slower                                                  |
| python_startup         | 10.8 ms                                                | 14.2 ms: 1.32x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.31x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.93 ms: 1.14x faster                                                  |
| django_template | 20.1 ms                                                | 19.4 ms: 1.04x faster                                                  |
| genshi_text     | 14.4 ms                                                | 14.0 ms: 1.03x faster                                                  |
| genshi_xml      | 28.5 ms                                                | 29.9 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 90.5 us: 3.33x faster                                                  |
| asyncio_tcp                | 643 ms                                                 | 428 ms: 1.50x faster                                                   |
| pylint                     | 253 ms                                                 | 168 ms: 1.50x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 237 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 195 ms: 1.42x faster                                                   |
| raytrace                   | 206 ms                                                 | 149 ms: 1.38x faster                                                   |
| chaos                      | 47.4 ms                                                | 34.8 ms: 1.36x faster                                                  |
| async_tree_none            | 282 ms                                                 | 207 ms: 1.36x faster                                                   |
| comprehensions             | 14.4 us                                                | 10.9 us: 1.32x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 255 ms: 1.32x faster                                                   |
| generators                 | 30.3 ms                                                | 23.1 ms: 1.31x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 557 ms: 1.30x faster                                                   |
| deltablue                  | 2.75 ms                                                | 2.15 ms: 1.28x faster                                                  |
| async_tree_io              | 697 ms                                                 | 558 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 451 ms: 1.22x faster                                                   |
| sqlglot_parse              | 890 us                                                 | 738 us: 1.21x faster                                                   |
| json_dumps                 | 7.53 ms                                                | 6.42 ms: 1.17x faster                                                  |
| sqlglot_transpile          | 1.05 ms                                                | 897 us: 1.17x faster                                                   |
| sympy_sum                  | 80.2 ms                                                | 69.7 ms: 1.15x faster                                                  |
| mako                       | 7.93 ms                                                | 6.93 ms: 1.14x faster                                                  |
| deepcopy_memo              | 25.7 us                                                | 22.6 us: 1.14x faster                                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.23 sec: 1.13x faster                                                 |
| hexiom                     | 4.58 ms                                                | 4.09 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 465 ms: 1.12x faster                                                   |
| logging_simple             | 3.41 us                                                | 3.07 us: 1.11x faster                                                  |
| logging_format             | 3.67 us                                                | 3.35 us: 1.10x faster                                                  |
| sympy_str                  | 144 ms                                                 | 131 ms: 1.09x faster                                                   |
| sympy_integrate            | 11.3 ms                                                | 10.4 ms: 1.08x faster                                                  |
| logging_silent             | 66.5 ns                                                | 61.6 ns: 1.08x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 178 us: 1.08x faster                                                   |
| nqueens                    | 55.9 ms                                                | 52.4 ms: 1.07x faster                                                  |
| coroutines                 | 17.2 ms                                                | 16.1 ms: 1.07x faster                                                  |
| regex_compile              | 72.8 ms                                                | 68.5 ms: 1.06x faster                                                  |
| richards_super             | 37.3 ms                                                | 35.2 ms: 1.06x faster                                                  |
| deepcopy                   | 215 us                                                 | 204 us: 1.06x faster                                                   |
| tornado_http               | 69.1 ms                                                | 65.4 ms: 1.06x faster                                                  |
| mdp                        | 1.48 sec                                               | 1.41 sec: 1.05x faster                                                 |
| html5lib                   | 33.0 ms                                                | 31.4 ms: 1.05x faster                                                  |
| go                         | 105 ms                                                 | 101 ms: 1.05x faster                                                   |
| unpickle_pure_python       | 149 us                                                 | 142 us: 1.04x faster                                                   |
| float                      | 50.8 ms                                                | 48.7 ms: 1.04x faster                                                  |
| django_template            | 20.1 ms                                                | 19.4 ms: 1.04x faster                                                  |
| dulwich_log                | 28.6 ms                                                | 27.5 ms: 1.04x faster                                                  |
| pprint_pformat             | 979 ms                                                 | 942 ms: 1.04x faster                                                   |
| pycparser                  | 659 ms                                                 | 639 ms: 1.03x faster                                                   |
| genshi_text                | 14.4 ms                                                | 14.0 ms: 1.03x faster                                                  |
| pprint_safe_repr           | 478 ms                                                 | 464 ms: 1.03x faster                                                   |
| gunicorn                   | 1.10 ms                                                | 1.06 ms: 1.03x faster                                                  |
| pathlib                    | 23.2 ms                                                | 22.5 ms: 1.03x faster                                                  |
| aiohttp                    | 1.02 ms                                                | 999 us: 1.03x faster                                                   |
| scimark_monte_carlo        | 43.5 ms                                                | 42.5 ms: 1.02x faster                                                  |
| meteor_contest             | 71.1 ms                                                | 70.0 ms: 1.01x faster                                                  |
| scimark_lu                 | 67.7 ms                                                | 66.8 ms: 1.01x faster                                                  |
| bench_thread_pool          | 465 us                                                 | 459 us: 1.01x faster                                                   |
| nbody                      | 61.7 ms                                                | 60.9 ms: 1.01x faster                                                  |
| sympy_expand               | 229 ms                                                 | 226 ms: 1.01x faster                                                   |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.80 ms: 1.00x faster                                                  |
| asyncio_websockets         | 408 ms                                                 | 409 ms: 1.00x slower                                                   |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                   |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| spectral_norm              | 65.7 ms                                                | 66.8 ms: 1.02x slower                                                  |
| mypy2                      | 372 ms                                                 | 379 ms: 1.02x slower                                                   |
| xml_etree_parse            | 100 ms                                                 | 102 ms: 1.02x slower                                                   |
| richards                   | 31.1 ms                                                | 31.8 ms: 1.02x slower                                                  |
| sqlglot_normalize          | 162 ms                                                 | 166 ms: 1.03x slower                                                   |
| coverage                   | 43.9 ms                                                | 45.1 ms: 1.03x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                                  |
| fannkuch                   | 240 ms                                                 | 249 ms: 1.04x slower                                                   |
| 2to3                       | 154 ms                                                 | 161 ms: 1.04x slower                                                   |
| sqlglot_optimize           | 29.6 ms                                                | 31.0 ms: 1.05x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 29.9 ms: 1.05x slower                                                  |
| xml_etree_iterparse        | 68.3 ms                                                | 71.7 ms: 1.05x slower                                                  |
| crypto_pyaes               | 47.5 ms                                                | 49.9 ms: 1.05x slower                                                  |
| regex_effbot               | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                  |
| scimark_fft                | 173 ms                                                 | 183 ms: 1.06x slower                                                   |
| thrift                     | 410 us                                                 | 435 us: 1.06x slower                                                   |
| json                       | 2.75 ms                                                | 2.95 ms: 1.07x slower                                                  |
| pickle                     | 6.98 us                                                | 7.49 us: 1.07x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.5 us: 1.08x slower                                                  |
| unpickle_list              | 2.69 us                                                | 2.91 us: 1.08x slower                                                  |
| pickle_list                | 2.70 us                                                | 2.99 us: 1.11x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.22 us: 1.11x slower                                                  |
| json_loads                 | 15.3 us                                                | 17.1 us: 1.11x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 37.3 ms: 1.11x slower                                                  |
| pyflate                    | 284 ms                                                 | 317 ms: 1.12x slower                                                   |
| tomli_loads                | 1.27 sec                                               | 1.44 sec: 1.13x slower                                                 |
| bench_mp_pool              | 41.0 ms                                                | 46.4 ms: 1.13x slower                                                  |
| xml_etree_generate         | 45.8 ms                                                | 52.3 ms: 1.14x slower                                                  |
| regex_v8                   | 15.1 ms                                                | 17.3 ms: 1.14x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 94.8 ms: 1.20x slower                                                  |
| sqlite_synth               | 1.26 us                                                | 1.53 us: 1.22x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 901 us: 1.27x slower                                                   |
| flaskblogging              | 2.35 ms                                                | 3.06 ms: 1.30x slower                                                  |
| python_startup_no_site     | 8.57 ms                                                | 11.2 ms: 1.31x slower                                                  |
| python_startup             | 10.8 ms                                                | 14.2 ms: 1.32x slower                                                  |
| telco                      | 3.17 ms                                                | 4.58 ms: 1.45x slower                                                  |
| async_generators           | 192 ms                                                 | 280 ms: 1.46x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (4): dask, docutils, deepcopy_reduce, chameleon
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240604-3.13.0b1+-6725c78/bm-20240604-darwin-arm64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 98.27% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.72x