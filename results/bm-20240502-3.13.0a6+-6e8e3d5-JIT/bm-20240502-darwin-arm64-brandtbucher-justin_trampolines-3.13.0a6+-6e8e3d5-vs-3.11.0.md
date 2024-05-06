# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_trampolines
- machine: darwin-arm64
- commit hash: 6e8e3d5
- commit date: 2024-05-02
- overall geometric mean: 1.01x faster
- HPT reliability: 61.50%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 154 ms                                                 | 170 ms: 1.10x slower                                                       |
| chameleon      | 4.30 ms                                                | 4.43 ms: 1.03x slower                                                      |
| docutils       | 1.43 sec                                               | 1.50 sec: 1.05x slower                                                     |
| html5lib       | 33.0 ms                                                | 30.9 ms: 1.07x faster                                                      |
| Geometric mean | (ref)                                                  | 1.03x slower                                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none_tg         | 276 ms                                                 | 195 ms: 1.42x faster                                                       |
| async_tree_none            | 282 ms                                                 | 200 ms: 1.41x faster                                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 258 ms: 1.37x faster                                                       |
| async_tree_io_tg           | 724 ms                                                 | 556 ms: 1.30x faster                                                       |
| async_tree_memoization     | 336 ms                                                 | 267 ms: 1.26x faster                                                       |
| async_tree_io              | 697 ms                                                 | 555 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 466 ms: 1.18x faster                                                       |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 460 ms: 1.13x faster                                                       |
| Geometric mean             | (ref)                                                  | 1.29x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 50.8 ms                                                | 49.4 ms: 1.03x faster                                                      |
| pidigits       | 280 ms                                                 | 282 ms: 1.01x slower                                                       |
| nbody          | 61.7 ms                                                | 67.8 ms: 1.10x slower                                                      |
| Geometric mean | (ref)                                                  | 1.02x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 72.8 ms                                                | 71.5 ms: 1.02x faster                                                      |
| regex_dna      | 148 ms                                                 | 149 ms: 1.01x slower                                                       |
| regex_effbot   | 2.43 ms                                                | 2.57 ms: 1.06x slower                                                      |
| regex_v8       | 15.1 ms                                                | 17.3 ms: 1.14x slower                                                      |
| Geometric mean | (ref)                                                  | 1.05x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 7.53 ms                                                | 6.32 ms: 1.19x faster                                                      |
| unpickle_pure_python | 149 us                                                 | 129 us: 1.15x faster                                                       |
| pickle_pure_python   | 191 us                                                 | 181 us: 1.06x faster                                                       |
| tomli_loads          | 1.27 sec                                               | 1.22 sec: 1.04x faster                                                     |
| xml_etree_iterparse  | 68.3 ms                                                | 69.9 ms: 1.02x slower                                                      |
| pickle               | 6.98 us                                                | 7.20 us: 1.03x slower                                                      |
| xml_etree_parse      | 100 ms                                                 | 104 ms: 1.04x slower                                                       |
| pickle_dict          | 17.1 us                                                | 18.1 us: 1.06x slower                                                      |
| xml_etree_process    | 33.6 ms                                                | 35.7 ms: 1.06x slower                                                      |
| unpickle_list        | 2.69 us                                                | 2.92 us: 1.09x slower                                                      |
| pickle_list          | 2.70 us                                                | 2.93 us: 1.09x slower                                                      |
| json_loads           | 15.3 us                                                | 17.0 us: 1.11x slower                                                      |
| unpickle             | 8.29 us                                                | 9.21 us: 1.11x slower                                                      |
| xml_etree_generate   | 45.8 ms                                                | 53.3 ms: 1.16x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                | 14.5 ms: 1.35x slower                                                      |
| python_startup_no_site | 8.57 ms                                                | 11.7 ms: 1.37x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 7.93 ms                                                | 6.39 ms: 1.24x faster                                                      |
| django_template | 20.1 ms                                                | 21.2 ms: 1.05x slower                                                      |
| genshi_text     | 14.4 ms                                                | 17.4 ms: 1.21x slower                                                      |
| genshi_xml      | 28.5 ms                                                | 40.6 ms: 1.42x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.10x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 301 us                                                 | 102 us: 2.96x faster                                                       |
| asyncio_tcp                | 643 ms                                                 | 422 ms: 1.52x faster                                                       |
| async_tree_none_tg         | 276 ms                                                 | 195 ms: 1.42x faster                                                       |
| async_tree_none            | 282 ms                                                 | 200 ms: 1.41x faster                                                       |
| pylint                     | 253 ms                                                 | 182 ms: 1.39x faster                                                       |
| async_tree_memoization_tg  | 352 ms                                                 | 258 ms: 1.37x faster                                                       |
| async_tree_io_tg           | 724 ms                                                 | 556 ms: 1.30x faster                                                       |
| generators                 | 30.3 ms                                                | 23.4 ms: 1.30x faster                                                      |
| async_tree_memoization     | 336 ms                                                 | 267 ms: 1.26x faster                                                       |
| async_tree_io              | 697 ms                                                 | 555 ms: 1.26x faster                                                       |
| mako                       | 7.93 ms                                                | 6.39 ms: 1.24x faster                                                      |
| raytrace                   | 206 ms                                                 | 170 ms: 1.21x faster                                                       |
| chaos                      | 47.4 ms                                                | 39.6 ms: 1.20x faster                                                      |
| json_dumps                 | 7.53 ms                                                | 6.32 ms: 1.19x faster                                                      |
| comprehensions             | 14.4 us                                                | 12.1 us: 1.19x faster                                                      |
| async_tree_cpu_io_mixed_tg | 550 ms                                                 | 466 ms: 1.18x faster                                                       |
| unpickle_pure_python       | 149 us                                                 | 129 us: 1.15x faster                                                       |
| sqlglot_parse              | 890 us                                                 | 777 us: 1.15x faster                                                       |
| deltablue                  | 2.75 ms                                                | 2.41 ms: 1.14x faster                                                      |
| richards_super             | 37.3 ms                                                | 32.9 ms: 1.13x faster                                                      |
| async_tree_cpu_io_mixed    | 519 ms                                                 | 460 ms: 1.13x faster                                                       |
| sqlglot_transpile          | 1.05 ms                                                | 943 us: 1.12x faster                                                       |
| sympy_sum                  | 80.2 ms                                                | 72.6 ms: 1.10x faster                                                      |
| deepcopy_memo              | 25.7 us                                                | 23.4 us: 1.10x faster                                                      |
| logging_simple             | 3.41 us                                                | 3.13 us: 1.09x faster                                                      |
| logging_format             | 3.67 us                                                | 3.41 us: 1.08x faster                                                      |
| html5lib                   | 33.0 ms                                                | 30.9 ms: 1.07x faster                                                      |
| pprint_safe_repr           | 478 ms                                                 | 449 ms: 1.06x faster                                                       |
| richards                   | 31.1 ms                                                | 29.2 ms: 1.06x faster                                                      |
| pprint_pformat             | 979 ms                                                 | 922 ms: 1.06x faster                                                       |
| pickle_pure_python         | 191 us                                                 | 181 us: 1.06x faster                                                       |
| coroutines                 | 17.2 ms                                                | 16.3 ms: 1.05x faster                                                      |
| logging_silent             | 66.5 ns                                                | 63.2 ns: 1.05x faster                                                      |
| asyncio_tcp_ssl            | 1.40 sec                                               | 1.33 sec: 1.05x faster                                                     |
| sympy_str                  | 144 ms                                                 | 137 ms: 1.05x faster                                                       |
| hexiom                     | 4.58 ms                                                | 4.36 ms: 1.05x faster                                                      |
| tomli_loads                | 1.27 sec                                               | 1.22 sec: 1.04x faster                                                     |
| sympy_integrate            | 11.3 ms                                                | 10.9 ms: 1.03x faster                                                      |
| float                      | 50.8 ms                                                | 49.4 ms: 1.03x faster                                                      |
| fannkuch                   | 240 ms                                                 | 233 ms: 1.03x faster                                                       |
| pycparser                  | 659 ms                                                 | 646 ms: 1.02x faster                                                       |
| deepcopy                   | 215 us                                                 | 211 us: 1.02x faster                                                       |
| regex_compile              | 72.8 ms                                                | 71.5 ms: 1.02x faster                                                      |
| go                         | 105 ms                                                 | 105 ms: 1.00x faster                                                       |
| scimark_monte_carlo        | 43.5 ms                                                | 43.7 ms: 1.00x slower                                                      |
| pidigits                   | 280 ms                                                 | 282 ms: 1.01x slower                                                       |
| regex_dna                  | 148 ms                                                 | 149 ms: 1.01x slower                                                       |
| dulwich_log                | 28.6 ms                                                | 29.0 ms: 1.01x slower                                                      |
| mdp                        | 1.48 sec                                               | 1.52 sec: 1.02x slower                                                     |
| meteor_contest             | 71.1 ms                                                | 72.5 ms: 1.02x slower                                                      |
| dask                       | 219 ms                                                 | 224 ms: 1.02x slower                                                       |
| xml_etree_iterparse        | 68.3 ms                                                | 69.9 ms: 1.02x slower                                                      |
| deepcopy_reduce            | 1.79 us                                                | 1.84 us: 1.03x slower                                                      |
| sympy_expand               | 229 ms                                                 | 235 ms: 1.03x slower                                                       |
| crypto_pyaes               | 47.5 ms                                                | 48.7 ms: 1.03x slower                                                      |
| nqueens                    | 55.9 ms                                                | 57.5 ms: 1.03x slower                                                      |
| chameleon                  | 4.30 ms                                                | 4.43 ms: 1.03x slower                                                      |
| gc_traversal               | 2.38 ms                                                | 2.46 ms: 1.03x slower                                                      |
| pickle                     | 6.98 us                                                | 7.20 us: 1.03x slower                                                      |
| bench_thread_pool          | 465 us                                                 | 481 us: 1.03x slower                                                       |
| coverage                   | 43.9 ms                                                | 45.4 ms: 1.03x slower                                                      |
| xml_etree_parse            | 100 ms                                                 | 104 ms: 1.04x slower                                                       |
| docutils                   | 1.43 sec                                               | 1.50 sec: 1.05x slower                                                     |
| django_template            | 20.1 ms                                                | 21.2 ms: 1.05x slower                                                      |
| regex_effbot               | 2.43 ms                                                | 2.57 ms: 1.06x slower                                                      |
| pickle_dict                | 17.1 us                                                | 18.1 us: 1.06x slower                                                      |
| scimark_sparse_mat_mult    | 2.81 ms                                                | 2.98 ms: 1.06x slower                                                      |
| xml_etree_process          | 33.6 ms                                                | 35.7 ms: 1.06x slower                                                      |
| spectral_norm              | 65.7 ms                                                | 70.1 ms: 1.07x slower                                                      |
| json                       | 2.75 ms                                                | 2.94 ms: 1.07x slower                                                      |
| sqlglot_normalize          | 162 ms                                                 | 174 ms: 1.08x slower                                                       |
| unpickle_list              | 2.69 us                                                | 2.92 us: 1.09x slower                                                      |
| pickle_list                | 2.70 us                                                | 2.93 us: 1.09x slower                                                      |
| thrift                     | 410 us                                                 | 447 us: 1.09x slower                                                       |
| aiohttp                    | 1.02 ms                                                | 1.12 ms: 1.09x slower                                                      |
| gunicorn                   | 1.10 ms                                                | 1.20 ms: 1.09x slower                                                      |
| nbody                      | 61.7 ms                                                | 67.8 ms: 1.10x slower                                                      |
| 2to3                       | 154 ms                                                 | 170 ms: 1.10x slower                                                       |
| json_loads                 | 15.3 us                                                | 17.0 us: 1.11x slower                                                      |
| pyflate                    | 284 ms                                                 | 314 ms: 1.11x slower                                                       |
| unpickle                   | 8.29 us                                                | 9.21 us: 1.11x slower                                                      |
| scimark_fft                | 173 ms                                                 | 192 ms: 1.11x slower                                                       |
| sqlglot_optimize           | 29.6 ms                                                | 33.1 ms: 1.12x slower                                                      |
| bench_mp_pool              | 41.0 ms                                                | 46.7 ms: 1.14x slower                                                      |
| regex_v8                   | 15.1 ms                                                | 17.3 ms: 1.14x slower                                                      |
| scimark_lu                 | 67.7 ms                                                | 78.8 ms: 1.16x slower                                                      |
| xml_etree_generate         | 45.8 ms                                                | 53.3 ms: 1.16x slower                                                      |
| genshi_text                | 14.4 ms                                                | 17.4 ms: 1.21x slower                                                      |
| sqlite_synth               | 1.26 us                                                | 1.58 us: 1.26x slower                                                      |
| create_gc_cycles           | 711 us                                                 | 906 us: 1.27x slower                                                       |
| scimark_sor                | 79.2 ms                                                | 103 ms: 1.30x slower                                                       |
| mypy2                      | 372 ms                                                 | 499 ms: 1.34x slower                                                       |
| python_startup             | 10.8 ms                                                | 14.5 ms: 1.35x slower                                                      |
| python_startup_no_site     | 8.57 ms                                                | 11.7 ms: 1.37x slower                                                      |
| telco                      | 3.17 ms                                                | 4.45 ms: 1.40x slower                                                      |
| genshi_xml                 | 28.5 ms                                                | 40.6 ms: 1.42x slower                                                      |
| async_generators           | 192 ms                                                 | 291 ms: 1.52x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (3): asyncio_websockets, pathlib, tornado_http
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (8) of results/bm-20240502-3.13.0a6+-6e8e3d5-JIT/bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg

# HPT report

- Reliability score: 61.50% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x