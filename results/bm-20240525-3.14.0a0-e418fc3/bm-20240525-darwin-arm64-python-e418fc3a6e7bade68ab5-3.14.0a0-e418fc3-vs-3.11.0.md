# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: darwin-arm64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.04x faster
- HPT reliability: 93.67%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.76x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 160 ms: 1.04x slower                                                  |
| chameleon      | 4.30 ms                                                | 4.33 ms: 1.01x slower                                                 |
| docutils       | 1.43 sec                                               | 1.44 sec: 1.00x slower                                                |
| html5lib       | 33.0 ms                                                | 31.1 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 238 ms: 1.48x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 196 ms: 1.41x faster                                                  |
| async_tree_none            | 282 ms                                                 | 214 ms: 1.32x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 562 ms: 1.29x faster                                                  |
| async_tree_memoization     | 336 ms                                                 | 264 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 450 ms: 1.22x faster                                                  |
| async_tree_io              | 697 ms                                                 | 577 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 474 ms: 1.10x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 48.7 ms: 1.04x faster                                                 |
| nbody          | 61.7 ms                                                | 59.9 ms: 1.03x faster                                                 |
| pidigits       | 280 ms                                                 | 281 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 68.3 ms: 1.07x faster                                                 |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| regex_effbot   | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                 |
| regex_v8       | 15.1 ms                                                | 17.7 ms: 1.17x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.32 ms: 1.19x faster                                                 |
| pickle_pure_python   | 191 us                                                 | 180 us: 1.06x faster                                                  |
| unpickle_pure_python | 149 us                                                 | 142 us: 1.05x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 103 ms: 1.03x slower                                                  |
| xml_etree_iterparse  | 68.3 ms                                                | 71.8 ms: 1.05x slower                                                 |
| pickle               | 6.98 us                                                | 7.36 us: 1.05x slower                                                 |
| unpickle_list        | 2.69 us                                                | 2.86 us: 1.07x slower                                                 |
| pickle_dict          | 17.1 us                                                | 18.2 us: 1.07x slower                                                 |
| xml_etree_process    | 33.6 ms                                                | 36.8 ms: 1.10x slower                                                 |
| json_loads           | 15.3 us                                                | 16.9 us: 1.10x slower                                                 |
| pickle_list          | 2.70 us                                                | 2.98 us: 1.10x slower                                                 |
| unpickle             | 8.29 us                                                | 9.28 us: 1.12x slower                                                 |
| xml_etree_generate   | 45.8 ms                                                | 51.8 ms: 1.13x slower                                                 |
| tomli_loads          | 1.27 sec                                               | 1.45 sec: 1.14x slower                                                |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 14.9 ms: 1.38x slower                                                 |
| python_startup_no_site | 8.57 ms                                                | 12.2 ms: 1.42x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.40x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 7.00 ms: 1.13x faster                                                 |
| genshi_text     | 14.4 ms                                                | 13.8 ms: 1.04x faster                                                 |
| django_template | 20.1 ms                                                | 19.6 ms: 1.03x faster                                                 |
| genshi_xml      | 28.5 ms                                                | 29.8 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 91.2 us: 3.30x faster                                                 |
| asyncio_tcp                | 643 ms                                                 | 421 ms: 1.53x faster                                                  |
| async_tree_memoization_tg  | 352 ms                                                 | 238 ms: 1.48x faster                                                  |
| pylint                     | 253 ms                                                 | 172 ms: 1.47x faster                                                  |
| async_tree_none_tg         | 276 ms                                                 | 196 ms: 1.41x faster                                                  |
| raytrace                   | 206 ms                                                 | 148 ms: 1.39x faster                                                  |
| comprehensions             | 14.4 us                                                | 10.7 us: 1.35x faster                                                 |
| chaos                      | 47.4 ms                                                | 35.5 ms: 1.33x faster                                                 |
| generators                 | 30.3 ms                                                | 22.8 ms: 1.33x faster                                                 |
| async_tree_none            | 282 ms                                                 | 214 ms: 1.32x faster                                                  |
| async_tree_io_tg           | 724 ms                                                 | 562 ms: 1.29x faster                                                  |
| deltablue                  | 2.75 ms                                                | 2.14 ms: 1.28x faster                                                 |
| async_tree_memoization     | 336 ms                                                 | 264 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 450 ms: 1.22x faster                                                  |
| sqlglot_parse              | 890 us                                                 | 732 us: 1.22x faster                                                  |
| async_tree_io              | 697 ms                                                 | 577 ms: 1.21x faster                                                  |
| json_dumps                 | 7.53 ms                                                | 6.32 ms: 1.19x faster                                                 |
| sqlglot_transpile          | 1.05 ms                                                | 892 us: 1.18x faster                                                  |
| sympy_sum                  | 80.2 ms                                                | 69.1 ms: 1.16x faster                                                 |
| deepcopy_memo              | 25.7 us                                                | 22.6 us: 1.14x faster                                                 |
| mako                       | 7.93 ms                                                | 7.00 ms: 1.13x faster                                                 |
| logging_simple             | 3.41 us                                                | 3.03 us: 1.13x faster                                                 |
| hexiom                     | 4.58 ms                                                | 4.08 ms: 1.12x faster                                                 |
| logging_silent             | 66.5 ns                                                | 60.0 ns: 1.11x faster                                                 |
| logging_format             | 3.67 us                                                | 3.32 us: 1.11x faster                                                 |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 474 ms: 1.10x faster                                                  |
| sympy_str                  | 144 ms                                                 | 131 ms: 1.09x faster                                                  |
| sympy_integrate            | 11.3 ms                                                | 10.4 ms: 1.09x faster                                                 |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.29 sec: 1.08x faster                                                |
| coroutines                 | 17.2 ms                                                | 15.9 ms: 1.08x faster                                                 |
| richards_super             | 37.3 ms                                                | 34.9 ms: 1.07x faster                                                 |
| regex_compile              | 72.8 ms                                                | 68.3 ms: 1.07x faster                                                 |
| deepcopy                   | 215 us                                                 | 202 us: 1.07x faster                                                  |
| pickle_pure_python         | 191 us                                                 | 180 us: 1.06x faster                                                  |
| pathlib                    | 23.2 ms                                                | 21.9 ms: 1.06x faster                                                 |
| html5lib                   | 33.0 ms                                                | 31.1 ms: 1.06x faster                                                 |
| nqueens                    | 55.9 ms                                                | 52.8 ms: 1.06x faster                                                 |
| go                         | 105 ms                                                 | 100 ms: 1.05x faster                                                  |
| unpickle_pure_python       | 149 us                                                 | 142 us: 1.05x faster                                                  |
| pprint_pformat             | 979 ms                                                 | 937 ms: 1.04x faster                                                  |
| float                      | 50.8 ms                                                | 48.7 ms: 1.04x faster                                                 |
| pycparser                  | 659 ms                                                 | 632 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 478 ms                                                 | 459 ms: 1.04x faster                                                  |
| genshi_text                | 14.4 ms                                                | 13.8 ms: 1.04x faster                                                 |
| nbody                      | 61.7 ms                                                | 59.9 ms: 1.03x faster                                                 |
| django_template            | 20.1 ms                                                | 19.6 ms: 1.03x faster                                                 |
| scimark_monte_carlo        | 43.5 ms                                                | 42.3 ms: 1.03x faster                                                 |
| scimark_lu                 | 67.7 ms                                                | 66.7 ms: 1.02x faster                                                 |
| sympy_expand               | 229 ms                                                 | 227 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.79 ms: 1.01x faster                                                 |
| meteor_contest             | 71.1 ms                                                | 70.4 ms: 1.01x faster                                                 |
| bench_thread_pool          | 465 us                                                 | 463 us: 1.00x faster                                                  |
| deepcopy_reduce            | 1.79 us                                                | 1.79 us: 1.00x faster                                                 |
| pidigits                   | 280 ms                                                 | 281 ms: 1.00x slower                                                  |
| docutils                   | 1.43 sec                                               | 1.44 sec: 1.00x slower                                                |
| chameleon                  | 4.30 ms                                                | 4.33 ms: 1.01x slower                                                 |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                  |
| spectral_norm              | 65.7 ms                                                | 67.2 ms: 1.02x slower                                                 |
| richards                   | 31.1 ms                                                | 31.9 ms: 1.03x slower                                                 |
| xml_etree_parse            | 100 ms                                                 | 103 ms: 1.03x slower                                                  |
| thrift                     | 410 us                                                 | 424 us: 1.03x slower                                                  |
| coverage                   | 43.9 ms                                                | 45.3 ms: 1.03x slower                                                 |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                                 |
| sqlglot_normalize          | 162 ms                                                 | 167 ms: 1.03x slower                                                  |
| 2to3                       | 154 ms                                                 | 160 ms: 1.04x slower                                                  |
| genshi_xml                 | 28.5 ms                                                | 29.8 ms: 1.04x slower                                                 |
| sqlglot_optimize           | 29.6 ms                                                | 31.0 ms: 1.05x slower                                                 |
| scimark_fft                | 173 ms                                                 | 181 ms: 1.05x slower                                                  |
| crypto_pyaes               | 47.5 ms                                                | 49.8 ms: 1.05x slower                                                 |
| xml_etree_iterparse        | 68.3 ms                                                | 71.8 ms: 1.05x slower                                                 |
| pickle                     | 6.98 us                                                | 7.36 us: 1.05x slower                                                 |
| regex_effbot               | 2.43 ms                                                | 2.56 ms: 1.06x slower                                                 |
| json                       | 2.75 ms                                                | 2.93 ms: 1.06x slower                                                 |
| unpickle_list              | 2.69 us                                                | 2.86 us: 1.07x slower                                                 |
| pickle_dict                | 17.1 us                                                | 18.2 us: 1.07x slower                                                 |
| fannkuch                   | 240 ms                                                 | 257 ms: 1.07x slower                                                  |
| xml_etree_process          | 33.6 ms                                                | 36.8 ms: 1.10x slower                                                 |
| json_loads                 | 15.3 us                                                | 16.9 us: 1.10x slower                                                 |
| pickle_list                | 2.70 us                                                | 2.98 us: 1.10x slower                                                 |
| unpickle                   | 8.29 us                                                | 9.28 us: 1.12x slower                                                 |
| xml_etree_generate         | 45.8 ms                                                | 51.8 ms: 1.13x slower                                                 |
| pyflate                    | 284 ms                                                 | 321 ms: 1.13x slower                                                  |
| bench_mp_pool              | 41.0 ms                                                | 46.5 ms: 1.13x slower                                                 |
| tomli_loads                | 1.27 sec                                               | 1.45 sec: 1.14x slower                                                |
| regex_v8                   | 15.1 ms                                                | 17.7 ms: 1.17x slower                                                 |
| scimark_sor                | 79.2 ms                                                | 95.4 ms: 1.20x slower                                                 |
| sqlite_synth               | 1.26 us                                                | 1.54 us: 1.22x slower                                                 |
| create_gc_cycles           | 711 us                                                 | 900 us: 1.27x slower                                                  |
| python_startup             | 10.8 ms                                                | 14.9 ms: 1.38x slower                                                 |
| python_startup_no_site     | 8.57 ms                                                | 12.2 ms: 1.42x slower                                                 |
| flaskblogging              | 2.35 ms                                                | 3.35 ms: 1.43x slower                                                 |
| telco                      | 3.17 ms                                                | 4.53 ms: 1.43x slower                                                 |
| async_generators           | 192 ms                                                 | 279 ms: 1.45x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (4): tornado_http, asyncio_websockets, mdp, dask
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dulwich_log, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240525-3.14.0a0-e418fc3/bm-20240525-darwin-arm64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 93.67% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.76x