# Results vs. 3.11.0

- fork: python
- ref: edb6883ef3f7a8ef0c83
- machine: darwin-arm64
- commit hash: edb6883
- commit date: 2024-06-01
- overall geometric mean: 1.05x faster
- HPT reliability: 99.39%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.64x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-darwin-arm64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 159 ms: 1.03x slower                                                   |
| html5lib       | 33.0 ms                                                | 31.1 ms: 1.06x faster                                                  |
| tornado_http   | 69.1 ms                                                | 65.5 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (2): chameleon, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-darwin-arm64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 235 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 195 ms: 1.42x faster                                                   |
| async_tree_none            | 282 ms                                                 | 206 ms: 1.37x faster                                                   |
| async_tree_memoization     | 336 ms                                                 | 255 ms: 1.32x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 554 ms: 1.31x faster                                                   |
| async_tree_io              | 697 ms                                                 | 551 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 446 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 462 ms: 1.12x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.31x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-darwin-arm64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 48.1 ms: 1.06x faster                                                  |
| nbody          | 61.7 ms                                                | 59.8 ms: 1.03x faster                                                  |
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-darwin-arm64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 68.0 ms: 1.07x faster                                                  |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                   |
| regex_effbot   | 2.43 ms                                                | 2.58 ms: 1.06x slower                                                  |
| regex_v8       | 15.1 ms                                                | 17.3 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-darwin-arm64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.18 ms: 1.22x faster                                                  |
| pickle_pure_python   | 191 us                                                 | 179 us: 1.07x faster                                                   |
| unpickle_pure_python | 149 us                                                 | 141 us: 1.06x faster                                                   |
| xml_etree_iterparse  | 68.3 ms                                                | 71.6 ms: 1.05x slower                                                  |
| xml_etree_parse      | 100 ms                                                 | 105 ms: 1.05x slower                                                   |
| unpickle_list        | 2.69 us                                                | 2.88 us: 1.07x slower                                                  |
| pickle               | 6.98 us                                                | 7.51 us: 1.08x slower                                                  |
| pickle_dict          | 17.1 us                                                | 18.6 us: 1.09x slower                                                  |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| xml_etree_process    | 33.6 ms                                                | 36.9 ms: 1.10x slower                                                  |
| unpickle             | 8.29 us                                                | 9.14 us: 1.10x slower                                                  |
| pickle_list          | 2.70 us                                                | 3.02 us: 1.12x slower                                                  |
| xml_etree_generate   | 45.8 ms                                                | 52.5 ms: 1.15x slower                                                  |
| tomli_loads          | 1.27 sec                                               | 1.46 sec: 1.15x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-darwin-arm64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 8.57 ms                                                | 10.3 ms: 1.20x slower                                                  |
| python_startup         | 10.8 ms                                                | 13.3 ms: 1.23x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-darwin-arm64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.97 ms: 1.14x faster                                                  |
| django_template | 20.1 ms                                                | 19.3 ms: 1.04x faster                                                  |
| genshi_text     | 14.4 ms                                                | 14.0 ms: 1.03x faster                                                  |
| genshi_xml      | 28.5 ms                                                | 30.2 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-darwin-arm64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 88.2 us: 3.41x faster                                                  |
| asyncio_tcp                | 643 ms                                                 | 389 ms: 1.65x faster                                                   |
| pylint                     | 253 ms                                                 | 168 ms: 1.51x faster                                                   |
| async_tree_memoization_tg  | 352 ms                                                 | 235 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 276 ms                                                 | 195 ms: 1.42x faster                                                   |
| comprehensions             | 14.4 us                                                | 10.2 us: 1.42x faster                                                  |
| raytrace                   | 206 ms                                                 | 147 ms: 1.40x faster                                                   |
| chaos                      | 47.4 ms                                                | 34.1 ms: 1.39x faster                                                  |
| async_tree_none            | 282 ms                                                 | 206 ms: 1.37x faster                                                   |
| generators                 | 30.3 ms                                                | 22.7 ms: 1.33x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 255 ms: 1.32x faster                                                   |
| async_tree_io_tg           | 724 ms                                                 | 554 ms: 1.31x faster                                                   |
| deltablue                  | 2.75 ms                                                | 2.14 ms: 1.29x faster                                                  |
| async_tree_io              | 697 ms                                                 | 551 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 446 ms: 1.23x faster                                                   |
| json_dumps                 | 7.53 ms                                                | 6.18 ms: 1.22x faster                                                  |
| sqlglot_parse              | 890 us                                                 | 731 us: 1.22x faster                                                   |
| sqlglot_transpile          | 1.05 ms                                                | 891 us: 1.18x faster                                                   |
| sympy_sum                  | 80.2 ms                                                | 69.0 ms: 1.16x faster                                                  |
| mako                       | 7.93 ms                                                | 6.97 ms: 1.14x faster                                                  |
| deepcopy_memo              | 25.7 us                                                | 22.6 us: 1.14x faster                                                  |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.23 sec: 1.14x faster                                                 |
| hexiom                     | 4.58 ms                                                | 4.07 ms: 1.12x faster                                                  |
| logging_simple             | 3.41 us                                                | 3.04 us: 1.12x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 462 ms: 1.12x faster                                                   |
| logging_format             | 3.67 us                                                | 3.32 us: 1.11x faster                                                  |
| logging_silent             | 66.5 ns                                                | 60.3 ns: 1.10x faster                                                  |
| sympy_str                  | 144 ms                                                 | 131 ms: 1.10x faster                                                   |
| sympy_integrate            | 11.3 ms                                                | 10.3 ms: 1.09x faster                                                  |
| coroutines                 | 17.2 ms                                                | 15.9 ms: 1.08x faster                                                  |
| regex_compile              | 72.8 ms                                                | 68.0 ms: 1.07x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 179 us: 1.07x faster                                                   |
| nqueens                    | 55.9 ms                                                | 52.6 ms: 1.06x faster                                                  |
| richards_super             | 37.3 ms                                                | 35.2 ms: 1.06x faster                                                  |
| html5lib                   | 33.0 ms                                                | 31.1 ms: 1.06x faster                                                  |
| float                      | 50.8 ms                                                | 48.1 ms: 1.06x faster                                                  |
| deepcopy                   | 215 us                                                 | 204 us: 1.06x faster                                                   |
| tornado_http               | 69.1 ms                                                | 65.5 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 149 us                                                 | 141 us: 1.06x faster                                                   |
| go                         | 105 ms                                                 | 100 ms: 1.05x faster                                                   |
| pathlib                    | 23.2 ms                                                | 22.1 ms: 1.05x faster                                                  |
| pprint_pformat             | 979 ms                                                 | 934 ms: 1.05x faster                                                   |
| pycparser                  | 659 ms                                                 | 631 ms: 1.04x faster                                                   |
| dulwich_log                | 28.6 ms                                                | 27.4 ms: 1.04x faster                                                  |
| django_template            | 20.1 ms                                                | 19.3 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 478 ms                                                 | 459 ms: 1.04x faster                                                   |
| nbody                      | 61.7 ms                                                | 59.8 ms: 1.03x faster                                                  |
| gunicorn                   | 1.10 ms                                                | 1.06 ms: 1.03x faster                                                  |
| scimark_monte_carlo        | 43.5 ms                                                | 42.4 ms: 1.03x faster                                                  |
| scimark_lu                 | 67.7 ms                                                | 66.0 ms: 1.03x faster                                                  |
| genshi_text                | 14.4 ms                                                | 14.0 ms: 1.03x faster                                                  |
| aiohttp                    | 1.02 ms                                                | 1.00 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.76 ms: 1.02x faster                                                  |
| sympy_expand               | 229 ms                                                 | 225 ms: 1.02x faster                                                   |
| bench_thread_pool          | 465 us                                                 | 457 us: 1.02x faster                                                   |
| meteor_contest             | 71.1 ms                                                | 70.2 ms: 1.01x faster                                                  |
| mdp                        | 1.48 sec                                               | 1.48 sec: 1.00x faster                                                 |
| asyncio_websockets         | 408 ms                                                 | 409 ms: 1.00x slower                                                   |
| deepcopy_reduce            | 1.79 us                                                | 1.80 us: 1.00x slower                                                  |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                   |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                   |
| spectral_norm              | 65.7 ms                                                | 66.3 ms: 1.01x slower                                                  |
| sqlglot_normalize          | 162 ms                                                 | 165 ms: 1.02x slower                                                   |
| richards                   | 31.1 ms                                                | 31.7 ms: 1.02x slower                                                  |
| coverage                   | 43.9 ms                                                | 44.9 ms: 1.02x slower                                                  |
| gc_traversal               | 2.38 ms                                                | 2.45 ms: 1.03x slower                                                  |
| fannkuch                   | 240 ms                                                 | 247 ms: 1.03x slower                                                   |
| 2to3                       | 154 ms                                                 | 159 ms: 1.03x slower                                                   |
| crypto_pyaes               | 47.5 ms                                                | 49.2 ms: 1.04x slower                                                  |
| scimark_fft                | 173 ms                                                 | 180 ms: 1.04x slower                                                   |
| sqlglot_optimize           | 29.6 ms                                                | 31.0 ms: 1.05x slower                                                  |
| thrift                     | 410 us                                                 | 430 us: 1.05x slower                                                   |
| xml_etree_iterparse        | 68.3 ms                                                | 71.6 ms: 1.05x slower                                                  |
| xml_etree_parse            | 100 ms                                                 | 105 ms: 1.05x slower                                                   |
| genshi_xml                 | 28.5 ms                                                | 30.2 ms: 1.06x slower                                                  |
| regex_effbot               | 2.43 ms                                                | 2.58 ms: 1.06x slower                                                  |
| json                       | 2.75 ms                                                | 2.93 ms: 1.06x slower                                                  |
| unpickle_list              | 2.69 us                                                | 2.88 us: 1.07x slower                                                  |
| pickle                     | 6.98 us                                                | 7.51 us: 1.08x slower                                                  |
| pickle_dict                | 17.1 us                                                | 18.6 us: 1.09x slower                                                  |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 36.9 ms: 1.10x slower                                                  |
| unpickle                   | 8.29 us                                                | 9.14 us: 1.10x slower                                                  |
| bench_mp_pool              | 41.0 ms                                                | 45.3 ms: 1.10x slower                                                  |
| pickle_list                | 2.70 us                                                | 3.02 us: 1.12x slower                                                  |
| pyflate                    | 284 ms                                                 | 318 ms: 1.12x slower                                                   |
| regex_v8                   | 15.1 ms                                                | 17.3 ms: 1.14x slower                                                  |
| xml_etree_generate         | 45.8 ms                                                | 52.5 ms: 1.15x slower                                                  |
| tomli_loads                | 1.27 sec                                               | 1.46 sec: 1.15x slower                                                 |
| python_startup_no_site     | 8.57 ms                                                | 10.3 ms: 1.20x slower                                                  |
| scimark_sor                | 79.2 ms                                                | 94.9 ms: 1.20x slower                                                  |
| sqlite_synth               | 1.26 us                                                | 1.54 us: 1.22x slower                                                  |
| python_startup             | 10.8 ms                                                | 13.3 ms: 1.23x slower                                                  |
| create_gc_cycles           | 711 us                                                 | 900 us: 1.27x slower                                                   |
| flaskblogging              | 2.35 ms                                                | 3.10 ms: 1.32x slower                                                  |
| telco                      | 3.17 ms                                                | 4.58 ms: 1.45x slower                                                  |
| async_generators           | 192 ms                                                 | 282 ms: 1.47x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (4): dask, docutils, chameleon, mypy2
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240601-3.13.0b1+-edb6883/bm-20240601-darwin-arm64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 99.39% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.64x