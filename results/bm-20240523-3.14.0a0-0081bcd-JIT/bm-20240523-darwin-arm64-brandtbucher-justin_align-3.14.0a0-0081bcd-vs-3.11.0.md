# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_align
- machine: darwin-arm64
- commit hash: 0081bcd
- commit date: 2024-05-23
- overall geometric mean: 1.02x faster
- HPT reliability: 57.39%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.74x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-darwin-arm64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 171 ms: 1.11x slower                                                |
| chameleon      | 4.30 ms                                                | 4.44 ms: 1.03x slower                                               |
| docutils       | 1.43 sec                                               | 1.52 sec: 1.06x slower                                              |
| html5lib       | 33.0 ms                                                | 30.8 ms: 1.07x faster                                               |
| Geometric mean | (ref)                                                  | 1.02x slower                                                        |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-darwin-arm64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_memoization_tg  | 352 ms                                                 | 241 ms: 1.46x faster                                                |
| async_tree_none_tg         | 276 ms                                                 | 199 ms: 1.39x faster                                                |
| async_tree_none            | 282 ms                                                 | 216 ms: 1.31x faster                                                |
| async_tree_io_tg           | 724 ms                                                 | 568 ms: 1.27x faster                                                |
| async_tree_memoization     | 336 ms                                                 | 266 ms: 1.26x faster                                                |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 453 ms: 1.21x faster                                                |
| async_tree_io              | 697 ms                                                 | 577 ms: 1.21x faster                                                |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 475 ms: 1.09x faster                                                |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-darwin-arm64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 47.2 ms: 1.08x faster                                               |
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                |
| nbody          | 61.7 ms                                                | 63.5 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                  | 1.01x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-darwin-arm64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 71.7 ms: 1.02x faster                                               |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                |
| regex_effbot   | 2.43 ms                                                | 2.57 ms: 1.06x slower                                               |
| regex_v8       | 15.1 ms                                                | 17.4 ms: 1.15x slower                                               |
| Geometric mean | (ref)                                                  | 1.05x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-darwin-arm64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.07 ms: 1.24x faster                                               |
| unpickle_pure_python | 149 us                                                 | 131 us: 1.13x faster                                                |
| pickle_pure_python   | 191 us                                                 | 172 us: 1.11x faster                                                |
| tomli_loads          | 1.27 sec                                               | 1.24 sec: 1.03x faster                                              |
| xml_etree_iterparse  | 68.3 ms                                                | 70.1 ms: 1.03x slower                                               |
| xml_etree_parse      | 100 ms                                                 | 103 ms: 1.03x slower                                                |
| xml_etree_process    | 33.6 ms                                                | 35.4 ms: 1.05x slower                                               |
| unpickle_list        | 2.69 us                                                | 2.83 us: 1.05x slower                                               |
| pickle_dict          | 17.1 us                                                | 18.1 us: 1.06x slower                                               |
| pickle               | 6.98 us                                                | 7.46 us: 1.07x slower                                               |
| pickle_list          | 2.70 us                                                | 2.98 us: 1.11x slower                                               |
| json_loads           | 15.3 us                                                | 17.0 us: 1.11x slower                                               |
| xml_etree_generate   | 45.8 ms                                                | 51.1 ms: 1.12x slower                                               |
| unpickle             | 8.29 us                                                | 9.32 us: 1.12x slower                                               |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-darwin-arm64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 15.7 ms: 1.46x slower                                               |
| python_startup_no_site | 8.57 ms                                                | 13.2 ms: 1.54x slower                                               |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-darwin-arm64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.40 ms: 1.24x faster                                               |
| django_template | 20.1 ms                                                | 21.0 ms: 1.05x slower                                               |
| genshi_text     | 14.4 ms                                                | 16.1 ms: 1.12x slower                                               |
| genshi_xml      | 28.5 ms                                                | 39.5 ms: 1.38x slower                                               |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-darwin-arm64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 93.5 us: 3.22x faster                                               |
| asyncio_tcp                | 643 ms                                                 | 416 ms: 1.55x faster                                                |
| async_tree_memoization_tg  | 352 ms                                                 | 241 ms: 1.46x faster                                                |
| async_tree_none_tg         | 276 ms                                                 | 199 ms: 1.39x faster                                                |
| pylint                     | 253 ms                                                 | 184 ms: 1.37x faster                                                |
| generators                 | 30.3 ms                                                | 23.2 ms: 1.31x faster                                               |
| async_tree_none            | 282 ms                                                 | 216 ms: 1.31x faster                                                |
| async_tree_io_tg           | 724 ms                                                 | 568 ms: 1.27x faster                                                |
| raytrace                   | 206 ms                                                 | 162 ms: 1.27x faster                                                |
| async_tree_memoization     | 336 ms                                                 | 266 ms: 1.26x faster                                                |
| json_dumps                 | 7.53 ms                                                | 6.07 ms: 1.24x faster                                               |
| mako                       | 7.93 ms                                                | 6.40 ms: 1.24x faster                                               |
| chaos                      | 47.4 ms                                                | 38.8 ms: 1.22x faster                                               |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 453 ms: 1.21x faster                                                |
| async_tree_io              | 697 ms                                                 | 577 ms: 1.21x faster                                                |
| deepcopy_memo              | 25.7 us                                                | 21.4 us: 1.21x faster                                               |
| comprehensions             | 14.4 us                                                | 12.2 us: 1.18x faster                                               |
| unpickle_pure_python       | 149 us                                                 | 131 us: 1.13x faster                                                |
| logging_simple             | 3.41 us                                                | 3.03 us: 1.13x faster                                               |
| deltablue                  | 2.75 ms                                                | 2.46 ms: 1.12x faster                                               |
| logging_format             | 3.67 us                                                | 3.29 us: 1.12x faster                                               |
| sympy_sum                  | 80.2 ms                                                | 71.9 ms: 1.11x faster                                               |
| pickle_pure_python         | 191 us                                                 | 172 us: 1.11x faster                                                |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 475 ms: 1.09x faster                                                |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.29 sec: 1.08x faster                                              |
| logging_silent             | 66.5 ns                                                | 61.8 ns: 1.08x faster                                               |
| float                      | 50.8 ms                                                | 47.2 ms: 1.08x faster                                               |
| coroutines                 | 17.2 ms                                                | 15.9 ms: 1.08x faster                                               |
| sqlglot_parse              | 890 us                                                 | 830 us: 1.07x faster                                                |
| html5lib                   | 33.0 ms                                                | 30.8 ms: 1.07x faster                                               |
| richards_super             | 37.3 ms                                                | 34.9 ms: 1.07x faster                                               |
| deepcopy                   | 215 us                                                 | 204 us: 1.06x faster                                                |
| sympy_str                  | 144 ms                                                 | 136 ms: 1.05x faster                                                |
| hexiom                     | 4.58 ms                                                | 4.36 ms: 1.05x faster                                               |
| sqlglot_transpile          | 1.05 ms                                                | 1.00 ms: 1.05x faster                                               |
| pprint_safe_repr           | 478 ms                                                 | 457 ms: 1.05x faster                                                |
| pathlib                    | 23.2 ms                                                | 22.2 ms: 1.04x faster                                               |
| sympy_integrate            | 11.3 ms                                                | 10.8 ms: 1.04x faster                                               |
| pprint_pformat             | 979 ms                                                 | 947 ms: 1.03x faster                                                |
| tomli_loads                | 1.27 sec                                               | 1.24 sec: 1.03x faster                                              |
| fannkuch                   | 240 ms                                                 | 234 ms: 1.02x faster                                                |
| go                         | 105 ms                                                 | 103 ms: 1.02x faster                                                |
| regex_compile              | 72.8 ms                                                | 71.7 ms: 1.02x faster                                               |
| richards                   | 31.1 ms                                                | 31.2 ms: 1.00x slower                                               |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                |
| meteor_contest             | 71.1 ms                                                | 71.5 ms: 1.01x slower                                               |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                |
| scimark_monte_carlo        | 43.5 ms                                                | 43.9 ms: 1.01x slower                                               |
| pycparser                  | 659 ms                                                 | 667 ms: 1.01x slower                                                |
| mdp                        | 1.48 sec                                               | 1.51 sec: 1.02x slower                                              |
| spectral_norm              | 65.7 ms                                                | 67.1 ms: 1.02x slower                                               |
| nqueens                    | 55.9 ms                                                | 57.2 ms: 1.02x slower                                               |
| xml_etree_iterparse        | 68.3 ms                                                | 70.1 ms: 1.03x slower                                               |
| sympy_expand               | 229 ms                                                 | 235 ms: 1.03x slower                                                |
| nbody                      | 61.7 ms                                                | 63.5 ms: 1.03x slower                                               |
| xml_etree_parse            | 100 ms                                                 | 103 ms: 1.03x slower                                                |
| coverage                   | 43.9 ms                                                | 45.3 ms: 1.03x slower                                               |
| chameleon                  | 4.30 ms                                                | 4.44 ms: 1.03x slower                                               |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.91 ms: 1.03x slower                                               |
| gc_traversal               | 2.38 ms                                                | 2.47 ms: 1.04x slower                                               |
| bench_thread_pool          | 465 us                                                 | 483 us: 1.04x slower                                                |
| django_template            | 20.1 ms                                                | 21.0 ms: 1.05x slower                                               |
| xml_etree_process          | 33.6 ms                                                | 35.4 ms: 1.05x slower                                               |
| unpickle_list              | 2.69 us                                                | 2.83 us: 1.05x slower                                               |
| thrift                     | 410 us                                                 | 434 us: 1.06x slower                                                |
| regex_effbot               | 2.43 ms                                                | 2.57 ms: 1.06x slower                                               |
| docutils                   | 1.43 sec                                               | 1.52 sec: 1.06x slower                                              |
| pickle_dict                | 17.1 us                                                | 18.1 us: 1.06x slower                                               |
| scimark_fft                | 173 ms                                                 | 184 ms: 1.07x slower                                                |
| json                       | 2.75 ms                                                | 2.94 ms: 1.07x slower                                               |
| pickle                     | 6.98 us                                                | 7.46 us: 1.07x slower                                               |
| crypto_pyaes               | 47.5 ms                                                | 51.9 ms: 1.09x slower                                               |
| pyflate                    | 284 ms                                                 | 312 ms: 1.10x slower                                                |
| sqlglot_optimize           | 29.6 ms                                                | 32.7 ms: 1.10x slower                                               |
| pickle_list                | 2.70 us                                                | 2.98 us: 1.11x slower                                               |
| json_loads                 | 15.3 us                                                | 17.0 us: 1.11x slower                                               |
| 2to3                       | 154 ms                                                 | 171 ms: 1.11x slower                                                |
| xml_etree_generate         | 45.8 ms                                                | 51.1 ms: 1.12x slower                                               |
| genshi_text                | 14.4 ms                                                | 16.1 ms: 1.12x slower                                               |
| unpickle                   | 8.29 us                                                | 9.32 us: 1.12x slower                                               |
| regex_v8                   | 15.1 ms                                                | 17.4 ms: 1.15x slower                                               |
| scimark_lu                 | 67.7 ms                                                | 78.2 ms: 1.15x slower                                               |
| bench_mp_pool              | 41.0 ms                                                | 49.6 ms: 1.21x slower                                               |
| sqlite_synth               | 1.26 us                                                | 1.56 us: 1.24x slower                                               |
| scimark_sor                | 79.2 ms                                                | 100 ms: 1.27x slower                                                |
| create_gc_cycles           | 711 us                                                 | 919 us: 1.29x slower                                                |
| genshi_xml                 | 28.5 ms                                                | 39.5 ms: 1.38x slower                                               |
| telco                      | 3.17 ms                                                | 4.55 ms: 1.44x slower                                               |
| python_startup             | 10.8 ms                                                | 15.7 ms: 1.46x slower                                               |
| flaskblogging              | 2.35 ms                                                | 3.53 ms: 1.50x slower                                               |
| async_generators           | 192 ms                                                 | 295 ms: 1.53x slower                                                |
| python_startup_no_site     | 8.57 ms                                                | 13.2 ms: 1.54x slower                                               |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                        |

Benchmark hidden because not significant (4): tornado_http, asyncio_websockets, deepcopy_reduce, dask
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dulwich_log, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
Ignored benchmarks (8) of results/bm-20240523-3.14.0a0-0081bcd-JIT/bm-20240523-darwin-arm64-brandtbucher-justin_align-3.14.0a0-0081bcd.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 57.39% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.74x