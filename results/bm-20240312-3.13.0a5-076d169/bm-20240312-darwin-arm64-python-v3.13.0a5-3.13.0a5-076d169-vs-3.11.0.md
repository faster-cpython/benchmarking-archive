# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a5
- machine: darwin-arm64
- commit hash: 076d169
- commit date: 2024-03-12
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 0.48x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 173 ms: 1.12x slower                                       |
| chameleon      | 4.30 ms                                                | 5.13 ms: 1.19x slower                                      |
| docutils       | 1.43 sec                                               | 1.47 sec: 1.03x slower                                     |
| html5lib       | 33.0 ms                                                | 35.5 ms: 1.08x slower                                      |
| Geometric mean | (ref)                                                  | 1.08x slower                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none            | 282 ms                                                 | 257 ms: 1.10x faster                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 323 ms: 1.09x faster                                       |
| async_tree_io_tg           | 724 ms                                                 | 672 ms: 1.08x faster                                       |
| async_tree_none_tg         | 276 ms                                                 | 259 ms: 1.07x faster                                       |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 531 ms: 1.04x faster                                       |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 525 ms: 1.01x slower                                       |
| async_tree_io              | 697 ms                                                 | 710 ms: 1.02x slower                                       |
| Geometric mean             | (ref)                                                  | 1.04x faster                                               |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                       |
| float          | 50.8 ms                                                | 57.0 ms: 1.12x slower                                      |
| nbody          | 61.7 ms                                                | 73.7 ms: 1.19x slower                                      |
| Geometric mean | (ref)                                                  | 1.11x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_dna      | 148 ms                                                 | 152 ms: 1.02x slower                                       |
| regex_compile  | 72.8 ms                                                | 75.1 ms: 1.03x slower                                      |
| regex_effbot   | 2.43 ms                                                | 2.56 ms: 1.06x slower                                      |
| regex_v8       | 15.1 ms                                                | 17.1 ms: 1.13x slower                                      |
| Geometric mean | (ref)                                                  | 1.06x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.52 ms: 1.16x faster                                      |
| pickle               | 6.98 us                                                | 7.31 us: 1.05x slower                                      |
| pickle_pure_python   | 191 us                                                 | 201 us: 1.05x slower                                       |
| unpickle_pure_python | 149 us                                                 | 157 us: 1.05x slower                                       |
| xml_etree_parse      | 100 ms                                                 | 106 ms: 1.06x slower                                       |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.07x slower                                      |
| pickle_list          | 2.70 us                                                | 2.96 us: 1.10x slower                                      |
| xml_etree_iterparse  | 68.3 ms                                                | 75.9 ms: 1.11x slower                                      |
| json_loads           | 15.3 us                                                | 17.1 us: 1.11x slower                                      |
| unpickle             | 8.29 us                                                | 9.30 us: 1.12x slower                                      |
| unpickle_list        | 2.69 us                                                | 3.05 us: 1.14x slower                                      |
| xml_etree_process    | 33.6 ms                                                | 40.4 ms: 1.20x slower                                      |
| tomli_loads          | 1.27 sec                                               | 1.55 sec: 1.22x slower                                     |
| xml_etree_generate   | 45.8 ms                                                | 58.1 ms: 1.27x slower                                      |
| Geometric mean       | (ref)                                                  | 1.10x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 12.9 ms: 1.20x slower                                      |
| python_startup_no_site | 8.57 ms                                                | 11.3 ms: 1.32x slower                                      |
| Geometric mean         | (ref)                                                  | 1.26x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| mako            | 7.93 ms                                                | 7.57 ms: 1.05x faster                                      |
| django_template | 20.1 ms                                                | 22.2 ms: 1.10x slower                                      |
| genshi_text     | 14.4 ms                                                | 15.9 ms: 1.10x slower                                      |
| genshi_xml      | 28.5 ms                                                | 33.8 ms: 1.18x slower                                      |
| Geometric mean  | (ref)                                                  | 1.08x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 72.9 us: 4.13x faster                                      |
| pylint                     | 253 ms                                                 | 171 ms: 1.47x faster                                       |
| asyncio_tcp                | 643 ms                                                 | 438 ms: 1.47x faster                                       |
| raytrace                   | 206 ms                                                 | 171 ms: 1.20x faster                                       |
| comprehensions             | 14.4 us                                                | 12.1 us: 1.20x faster                                      |
| chaos                      | 47.4 ms                                                | 39.9 ms: 1.19x faster                                      |
| json_dumps                 | 7.53 ms                                                | 6.52 ms: 1.16x faster                                      |
| deltablue                  | 2.75 ms                                                | 2.45 ms: 1.12x faster                                      |
| sqlglot_parse              | 890 us                                                 | 795 us: 1.12x faster                                       |
| async_tree_none            | 282 ms                                                 | 257 ms: 1.10x faster                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 323 ms: 1.09x faster                                       |
| sqlglot_transpile          | 1.05 ms                                                | 972 us: 1.08x faster                                       |
| async_tree_io_tg           | 724 ms                                                 | 672 ms: 1.08x faster                                       |
| sympy_sum                  | 80.2 ms                                                | 75.0 ms: 1.07x faster                                      |
| async_tree_none_tg         | 276 ms                                                 | 259 ms: 1.07x faster                                       |
| generators                 | 30.3 ms                                                | 28.6 ms: 1.06x faster                                      |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.32 sec: 1.05x faster                                     |
| mako                       | 7.93 ms                                                | 7.57 ms: 1.05x faster                                      |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 531 ms: 1.04x faster                                       |
| sympy_integrate            | 11.3 ms                                                | 10.9 ms: 1.03x faster                                      |
| sympy_str                  | 144 ms                                                 | 143 ms: 1.00x faster                                       |
| go                         | 105 ms                                                 | 105 ms: 1.00x faster                                       |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                       |
| deepcopy_memo              | 25.7 us                                                | 25.9 us: 1.01x slower                                      |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 525 ms: 1.01x slower                                       |
| gc_traversal               | 2.38 ms                                                | 2.42 ms: 1.01x slower                                      |
| richards_super             | 37.3 ms                                                | 38.0 ms: 1.02x slower                                      |
| async_tree_io              | 697 ms                                                 | 710 ms: 1.02x slower                                       |
| regex_dna                  | 148 ms                                                 | 152 ms: 1.02x slower                                       |
| crypto_pyaes               | 47.5 ms                                                | 48.7 ms: 1.03x slower                                      |
| logging_simple             | 3.41 us                                                | 3.50 us: 1.03x slower                                      |
| docutils                   | 1.43 sec                                               | 1.47 sec: 1.03x slower                                     |
| dask                       | 219 ms                                                 | 225 ms: 1.03x slower                                       |
| aiohttp                    | 1.02 ms                                                | 1.06 ms: 1.03x slower                                      |
| regex_compile              | 72.8 ms                                                | 75.1 ms: 1.03x slower                                      |
| logging_format             | 3.67 us                                                | 3.80 us: 1.03x slower                                      |
| dulwich_log                | 28.6 ms                                                | 29.6 ms: 1.03x slower                                      |
| meteor_contest             | 71.1 ms                                                | 73.6 ms: 1.04x slower                                      |
| pickle                     | 6.98 us                                                | 7.31 us: 1.05x slower                                      |
| pickle_pure_python         | 191 us                                                 | 201 us: 1.05x slower                                       |
| logging_silent             | 66.5 ns                                                | 70.0 ns: 1.05x slower                                      |
| unpickle_pure_python       | 149 us                                                 | 157 us: 1.05x slower                                       |
| hexiom                     | 4.58 ms                                                | 4.83 ms: 1.05x slower                                      |
| regex_effbot               | 2.43 ms                                                | 2.56 ms: 1.06x slower                                      |
| xml_etree_parse            | 100 ms                                                 | 106 ms: 1.06x slower                                       |
| pycparser                  | 659 ms                                                 | 700 ms: 1.06x slower                                       |
| sympy_expand               | 229 ms                                                 | 243 ms: 1.06x slower                                       |
| bench_thread_pool          | 465 us                                                 | 495 us: 1.06x slower                                       |
| deepcopy                   | 215 us                                                 | 230 us: 1.07x slower                                       |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.07x slower                                      |
| pathlib                    | 23.2 ms                                                | 24.8 ms: 1.07x slower                                      |
| json                       | 2.75 ms                                                | 2.95 ms: 1.07x slower                                      |
| html5lib                   | 33.0 ms                                                | 35.5 ms: 1.08x slower                                      |
| pprint_pformat             | 979 ms                                                 | 1.06 sec: 1.08x slower                                     |
| pprint_safe_repr           | 478 ms                                                 | 522 ms: 1.09x slower                                       |
| scimark_lu                 | 67.7 ms                                                | 74.3 ms: 1.10x slower                                      |
| pickle_list                | 2.70 us                                                | 2.96 us: 1.10x slower                                      |
| django_template            | 20.1 ms                                                | 22.2 ms: 1.10x slower                                      |
| thrift                     | 410 us                                                 | 452 us: 1.10x slower                                       |
| coverage                   | 43.9 ms                                                | 48.4 ms: 1.10x slower                                      |
| genshi_text                | 14.4 ms                                                | 15.9 ms: 1.10x slower                                      |
| mdp                        | 1.48 sec                                               | 1.64 sec: 1.11x slower                                     |
| bench_mp_pool              | 41.0 ms                                                | 45.4 ms: 1.11x slower                                      |
| scimark_monte_carlo        | 43.5 ms                                                | 48.3 ms: 1.11x slower                                      |
| richards                   | 31.1 ms                                                | 34.5 ms: 1.11x slower                                      |
| xml_etree_iterparse        | 68.3 ms                                                | 75.9 ms: 1.11x slower                                      |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.13 ms: 1.11x slower                                      |
| json_loads                 | 15.3 us                                                | 17.1 us: 1.11x slower                                      |
| coroutines                 | 17.2 ms                                                | 19.2 ms: 1.12x slower                                      |
| 2to3                       | 154 ms                                                 | 173 ms: 1.12x slower                                       |
| float                      | 50.8 ms                                                | 57.0 ms: 1.12x slower                                      |
| unpickle                   | 8.29 us                                                | 9.30 us: 1.12x slower                                      |
| regex_v8                   | 15.1 ms                                                | 17.1 ms: 1.13x slower                                      |
| unpickle_list              | 2.69 us                                                | 3.05 us: 1.14x slower                                      |
| sqlglot_normalize          | 162 ms                                                 | 185 ms: 1.14x slower                                       |
| fannkuch                   | 240 ms                                                 | 274 ms: 1.14x slower                                       |
| deepcopy_reduce            | 1.79 us                                                | 2.06 us: 1.15x slower                                      |
| sqlglot_optimize           | 29.6 ms                                                | 34.2 ms: 1.15x slower                                      |
| spectral_norm              | 65.7 ms                                                | 75.8 ms: 1.15x slower                                      |
| nqueens                    | 55.9 ms                                                | 65.2 ms: 1.17x slower                                      |
| genshi_xml                 | 28.5 ms                                                | 33.8 ms: 1.18x slower                                      |
| chameleon                  | 4.30 ms                                                | 5.13 ms: 1.19x slower                                      |
| nbody                      | 61.7 ms                                                | 73.7 ms: 1.19x slower                                      |
| scimark_fft                | 173 ms                                                 | 207 ms: 1.20x slower                                       |
| python_startup             | 10.8 ms                                                | 12.9 ms: 1.20x slower                                      |
| xml_etree_process          | 33.6 ms                                                | 40.4 ms: 1.20x slower                                      |
| pyflate                    | 284 ms                                                 | 342 ms: 1.20x slower                                       |
| tomli_loads                | 1.27 sec                                               | 1.55 sec: 1.22x slower                                     |
| mypy2                      | 372 ms                                                 | 457 ms: 1.23x slower                                       |
| sqlite_synth               | 1.26 us                                                | 1.57 us: 1.25x slower                                      |
| xml_etree_generate         | 45.8 ms                                                | 58.1 ms: 1.27x slower                                      |
| python_startup_no_site     | 8.57 ms                                                | 11.3 ms: 1.32x slower                                      |
| scimark_sor                | 79.2 ms                                                | 105 ms: 1.33x slower                                       |
| flaskblogging              | 2.35 ms                                                | 3.40 ms: 1.45x slower                                      |
| telco                      | 3.17 ms                                                | 4.63 ms: 1.46x slower                                      |
| async_generators           | 192 ms                                                 | 302 ms: 1.57x slower                                       |
| Geometric mean             | (ref)                                                  | 1.04x slower                                               |

Benchmark hidden because not significant (5): gunicorn, tornado_http, async_tree_memoization, create_gc_cycles, asyncio_websockets
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240312-3.13.0a5-076d169/bm-20240312-darwin-arm64-python-v3.13.0a5-3.13.0a5-076d169.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 0.48x