# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a3
- machine: darwin-arm64
- commit hash: f009305
- commit date: 2024-01-17
- overall geometric mean: 1.05x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 170 ms: 1.10x slower                                       |
| chameleon      | 4.30 ms                                                | 4.87 ms: 1.13x slower                                      |
| docutils       | 1.43 sec                                               | 1.46 sec: 1.02x slower                                     |
| html5lib       | 33.0 ms                                                | 35.9 ms: 1.09x slower                                      |
| tornado_http   | 69.1 ms                                                | 78.1 ms: 1.13x slower                                      |
| Geometric mean | (ref)                                                  | 1.09x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_none            | 282 ms                                                 | 253 ms: 1.11x faster                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 324 ms: 1.09x faster                                       |
| async_tree_io_tg           | 724 ms                                                 | 672 ms: 1.08x faster                                       |
| async_tree_none_tg         | 276 ms                                                 | 260 ms: 1.06x faster                                       |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 531 ms: 1.03x faster                                       |
| async_tree_io              | 697 ms                                                 | 703 ms: 1.01x slower                                       |
| Geometric mean             | (ref)                                                  | 1.05x faster                                               |

Benchmark hidden because not significant (2): async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                       |
| float          | 50.8 ms                                                | 56.9 ms: 1.12x slower                                      |
| nbody          | 61.7 ms                                                | 75.6 ms: 1.22x slower                                      |
| Geometric mean | (ref)                                                  | 1.11x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 73.8 ms: 1.01x slower                                      |
| regex_dna      | 148 ms                                                 | 157 ms: 1.06x slower                                       |
| regex_effbot   | 2.43 ms                                                | 2.77 ms: 1.14x slower                                      |
| regex_v8       | 15.1 ms                                                | 18.0 ms: 1.19x slower                                      |
| Geometric mean | (ref)                                                  | 1.10x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.52 ms: 1.16x faster                                      |
| xml_etree_parse      | 100 ms                                                 | 99.6 ms: 1.01x faster                                      |
| pickle_pure_python   | 191 us                                                 | 198 us: 1.03x slower                                       |
| unpickle_pure_python | 149 us                                                 | 154 us: 1.04x slower                                       |
| xml_etree_iterparse  | 68.3 ms                                                | 71.9 ms: 1.05x slower                                      |
| pickle               | 6.98 us                                                | 7.41 us: 1.06x slower                                      |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.06x slower                                      |
| pickle_list          | 2.70 us                                                | 2.93 us: 1.09x slower                                      |
| json_loads           | 15.3 us                                                | 17.1 us: 1.11x slower                                      |
| unpickle             | 8.29 us                                                | 9.29 us: 1.12x slower                                      |
| unpickle_list        | 2.69 us                                                | 3.11 us: 1.16x slower                                      |
| xml_etree_process    | 33.6 ms                                                | 39.9 ms: 1.19x slower                                      |
| tomli_loads          | 1.27 sec                                               | 1.54 sec: 1.21x slower                                     |
| xml_etree_generate   | 45.8 ms                                                | 56.3 ms: 1.23x slower                                      |
| Geometric mean       | (ref)                                                  | 1.08x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 13.9 ms: 1.29x slower                                      |
| python_startup_no_site | 8.57 ms                                                | 12.3 ms: 1.44x slower                                      |
| Geometric mean         | (ref)                                                  | 1.36x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| mako            | 7.93 ms                                                | 7.54 ms: 1.05x faster                                      |
| django_template | 20.1 ms                                                | 21.7 ms: 1.08x slower                                      |
| genshi_text     | 14.4 ms                                                | 15.8 ms: 1.10x slower                                      |
| genshi_xml      | 28.5 ms                                                | 33.6 ms: 1.18x slower                                      |
| Geometric mean  | (ref)                                                  | 1.07x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 70.9 us: 4.24x faster                                      |
| asyncio_tcp                | 643 ms                                                 | 404 ms: 1.59x faster                                       |
| pylint                     | 253 ms                                                 | 169 ms: 1.50x faster                                       |
| raytrace                   | 206 ms                                                 | 171 ms: 1.20x faster                                       |
| comprehensions             | 14.4 us                                                | 12.1 us: 1.19x faster                                      |
| chaos                      | 47.4 ms                                                | 39.8 ms: 1.19x faster                                      |
| json_dumps                 | 7.53 ms                                                | 6.52 ms: 1.16x faster                                      |
| sqlglot_parse              | 890 us                                                 | 789 us: 1.13x faster                                       |
| deltablue                  | 2.75 ms                                                | 2.44 ms: 1.13x faster                                      |
| async_tree_none            | 282 ms                                                 | 253 ms: 1.11x faster                                       |
| sympy_sum                  | 80.2 ms                                                | 72.5 ms: 1.11x faster                                      |
| sqlglot_transpile          | 1.05 ms                                                | 965 us: 1.09x faster                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 324 ms: 1.09x faster                                       |
| async_tree_io_tg           | 724 ms                                                 | 672 ms: 1.08x faster                                       |
| generators                 | 30.3 ms                                                | 28.4 ms: 1.07x faster                                      |
| async_tree_none_tg         | 276 ms                                                 | 260 ms: 1.06x faster                                       |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.32 sec: 1.05x faster                                     |
| mako                       | 7.93 ms                                                | 7.54 ms: 1.05x faster                                      |
| sympy_integrate            | 11.3 ms                                                | 10.7 ms: 1.05x faster                                      |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 531 ms: 1.03x faster                                       |
| sympy_str                  | 144 ms                                                 | 140 ms: 1.03x faster                                       |
| xml_etree_parse            | 100 ms                                                 | 99.6 ms: 1.01x faster                                      |
| create_gc_cycles           | 711 us                                                 | 706 us: 1.01x faster                                       |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                       |
| gc_traversal               | 2.38 ms                                                | 2.40 ms: 1.01x slower                                      |
| async_tree_io              | 697 ms                                                 | 703 ms: 1.01x slower                                       |
| regex_compile              | 72.8 ms                                                | 73.8 ms: 1.01x slower                                      |
| crypto_pyaes               | 47.5 ms                                                | 48.3 ms: 1.02x slower                                      |
| docutils                   | 1.43 sec                                               | 1.46 sec: 1.02x slower                                     |
| logging_simple             | 3.41 us                                                | 3.49 us: 1.02x slower                                      |
| meteor_contest             | 71.1 ms                                                | 72.7 ms: 1.02x slower                                      |
| dulwich_log                | 28.6 ms                                                | 29.4 ms: 1.03x slower                                      |
| logging_format             | 3.67 us                                                | 3.79 us: 1.03x slower                                      |
| pickle_pure_python         | 191 us                                                 | 198 us: 1.03x slower                                       |
| unpickle_pure_python       | 149 us                                                 | 154 us: 1.04x slower                                       |
| sympy_expand               | 229 ms                                                 | 238 ms: 1.04x slower                                       |
| deepcopy                   | 215 us                                                 | 225 us: 1.05x slower                                       |
| logging_silent             | 66.5 ns                                                | 69.9 ns: 1.05x slower                                      |
| mdp                        | 1.48 sec                                               | 1.56 sec: 1.05x slower                                     |
| xml_etree_iterparse        | 68.3 ms                                                | 71.9 ms: 1.05x slower                                      |
| pathlib                    | 23.2 ms                                                | 24.5 ms: 1.05x slower                                      |
| regex_dna                  | 148 ms                                                 | 157 ms: 1.06x slower                                       |
| pickle                     | 6.98 us                                                | 7.41 us: 1.06x slower                                      |
| pycparser                  | 659 ms                                                 | 700 ms: 1.06x slower                                       |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.06x slower                                      |
| pprint_pformat             | 979 ms                                                 | 1.05 sec: 1.07x slower                                     |
| bench_thread_pool          | 465 us                                                 | 500 us: 1.07x slower                                       |
| coverage                   | 43.9 ms                                                | 47.2 ms: 1.08x slower                                      |
| django_template            | 20.1 ms                                                | 21.7 ms: 1.08x slower                                      |
| pprint_safe_repr           | 478 ms                                                 | 516 ms: 1.08x slower                                       |
| json                       | 2.75 ms                                                | 2.98 ms: 1.08x slower                                      |
| pickle_list                | 2.70 us                                                | 2.93 us: 1.09x slower                                      |
| coroutines                 | 17.2 ms                                                | 18.7 ms: 1.09x slower                                      |
| nqueens                    | 55.9 ms                                                | 60.9 ms: 1.09x slower                                      |
| richards                   | 31.1 ms                                                | 33.8 ms: 1.09x slower                                      |
| html5lib                   | 33.0 ms                                                | 35.9 ms: 1.09x slower                                      |
| scimark_monte_carlo        | 43.5 ms                                                | 47.5 ms: 1.09x slower                                      |
| genshi_text                | 14.4 ms                                                | 15.8 ms: 1.10x slower                                      |
| scimark_lu                 | 67.7 ms                                                | 74.2 ms: 1.10x slower                                      |
| bench_mp_pool              | 41.0 ms                                                | 45.1 ms: 1.10x slower                                      |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 3.11 ms: 1.10x slower                                      |
| 2to3                       | 154 ms                                                 | 170 ms: 1.10x slower                                       |
| deepcopy_reduce            | 1.79 us                                                | 1.98 us: 1.10x slower                                      |
| json_loads                 | 15.3 us                                                | 17.1 us: 1.11x slower                                      |
| thrift                     | 410 us                                                 | 458 us: 1.12x slower                                       |
| unpickle                   | 8.29 us                                                | 9.29 us: 1.12x slower                                      |
| float                      | 50.8 ms                                                | 56.9 ms: 1.12x slower                                      |
| sqlglot_normalize          | 162 ms                                                 | 183 ms: 1.13x slower                                       |
| tornado_http               | 69.1 ms                                                | 78.1 ms: 1.13x slower                                      |
| chameleon                  | 4.30 ms                                                | 4.87 ms: 1.13x slower                                      |
| fannkuch                   | 240 ms                                                 | 273 ms: 1.14x slower                                       |
| regex_effbot               | 2.43 ms                                                | 2.77 ms: 1.14x slower                                      |
| sqlglot_optimize           | 29.6 ms                                                | 33.9 ms: 1.15x slower                                      |
| spectral_norm              | 65.7 ms                                                | 75.4 ms: 1.15x slower                                      |
| unpickle_list              | 2.69 us                                                | 3.11 us: 1.16x slower                                      |
| genshi_xml                 | 28.5 ms                                                | 33.6 ms: 1.18x slower                                      |
| gunicorn                   | 1.10 ms                                                | 1.30 ms: 1.18x slower                                      |
| scimark_fft                | 173 ms                                                 | 204 ms: 1.18x slower                                       |
| regex_v8                   | 15.1 ms                                                | 18.0 ms: 1.19x slower                                      |
| xml_etree_process          | 33.6 ms                                                | 39.9 ms: 1.19x slower                                      |
| pyflate                    | 284 ms                                                 | 339 ms: 1.20x slower                                       |
| tomli_loads                | 1.27 sec                                               | 1.54 sec: 1.21x slower                                     |
| aiohttp                    | 1.02 ms                                                | 1.25 ms: 1.22x slower                                      |
| nbody                      | 61.7 ms                                                | 75.6 ms: 1.22x slower                                      |
| xml_etree_generate         | 45.8 ms                                                | 56.3 ms: 1.23x slower                                      |
| sqlite_synth               | 1.26 us                                                | 1.60 us: 1.28x slower                                      |
| python_startup             | 10.8 ms                                                | 13.9 ms: 1.29x slower                                      |
| scimark_sor                | 79.2 ms                                                | 105 ms: 1.33x slower                                       |
| python_startup_no_site     | 8.57 ms                                                | 12.3 ms: 1.44x slower                                      |
| telco                      | 3.17 ms                                                | 4.65 ms: 1.47x slower                                      |
| async_generators           | 192 ms                                                 | 296 ms: 1.54x slower                                       |
| mypy2                      | 372 ms                                                 | 597 ms: 1.60x slower                                       |
| flaskblogging              | 2.35 ms                                                | 3.94 ms: 1.68x slower                                      |
| Geometric mean             | (ref)                                                  | 1.05x slower                                               |

Benchmark hidden because not significant (7): async_tree_memoization, deepcopy_memo, hexiom, richards_super, asyncio_websockets, go, async_tree_cpu_io_mixed
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240117-3.13.0a3-f009305/bm-20240117-darwin-arm64-python-v3.13.0a3-3.13.0a3-f009305.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.04x