# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_trampolines
- machine: darwin-arm64
- commit hash: 6e8e3d5
- commit date: 2024-05-02
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 170 ms: 1.00x slower                                                       |
| chameleon      | 4.70 ms                                                | 4.43 ms: 1.06x faster                                                      |
| Geometric mean | (ref)                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none            | 266 ms                                                 | 200 ms: 1.33x faster                                                       |
| async_tree_none_tg         | 258 ms                                                 | 195 ms: 1.32x faster                                                       |
| async_tree_memoization_tg  | 323 ms                                                 | 258 ms: 1.25x faster                                                       |
| async_tree_io              | 668 ms                                                 | 555 ms: 1.20x faster                                                       |
| async_tree_io_tg           | 669 ms                                                 | 556 ms: 1.20x faster                                                       |
| async_tree_memoization     | 312 ms                                                 | 267 ms: 1.17x faster                                                       |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 466 ms: 1.14x faster                                                       |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 460 ms: 1.14x faster                                                       |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 49.4 ms: 1.13x faster                                                      |
| nbody          | 68.8 ms                                                | 67.8 ms: 1.02x faster                                                      |
| pidigits       | 282 ms                                                 | 282 ms: 1.00x slower                                                       |
| Geometric mean | (ref)                                                  | 1.05x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 77.9 ms                                                | 71.5 ms: 1.09x faster                                                      |
| regex_dna      | 154 ms                                                 | 149 ms: 1.03x faster                                                       |
| regex_effbot   | 2.64 ms                                                | 2.57 ms: 1.03x faster                                                      |
| regex_v8       | 16.0 ms                                                | 17.3 ms: 1.09x slower                                                      |
| Geometric mean | (ref)                                                  | 1.02x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle_pure_python | 151 us                                                 | 129 us: 1.17x faster                                                       |
| tomli_loads          | 1.39 sec                                               | 1.22 sec: 1.14x faster                                                     |
| xml_etree_process    | 39.7 ms                                                | 35.7 ms: 1.11x faster                                                      |
| pickle_pure_python   | 200 us                                                 | 181 us: 1.10x faster                                                       |
| xml_etree_iterparse  | 74.0 ms                                                | 69.9 ms: 1.06x faster                                                      |
| xml_etree_generate   | 55.8 ms                                                | 53.3 ms: 1.05x faster                                                      |
| unpickle_list        | 3.02 us                                                | 2.92 us: 1.04x faster                                                      |
| xml_etree_parse      | 106 ms                                                 | 104 ms: 1.02x faster                                                       |
| json_loads           | 17.2 us                                                | 17.0 us: 1.02x faster                                                      |
| pickle               | 7.23 us                                                | 7.20 us: 1.00x faster                                                      |
| pickle_dict          | 18.1 us                                                | 18.1 us: 1.00x slower                                                      |
| unpickle             | 9.12 us                                                | 9.21 us: 1.01x slower                                                      |
| pickle_list          | 2.89 us                                                | 2.93 us: 1.01x slower                                                      |
| json_dumps           | 6.22 ms                                                | 6.32 ms: 1.02x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 9.37 ms                                                | 11.7 ms: 1.25x slower                                                      |
| python_startup         | 11.4 ms                                                | 14.5 ms: 1.27x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 7.71 ms                                                | 6.39 ms: 1.21x faster                                                      |
| django_template | 22.3 ms                                                | 21.2 ms: 1.06x faster                                                      |
| Geometric mean  | (ref)                                                  | 1.13x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| generators                 | 31.1 ms                                                | 23.4 ms: 1.33x faster                                                      |
| async_tree_none            | 266 ms                                                 | 200 ms: 1.33x faster                                                       |
| async_tree_none_tg         | 258 ms                                                 | 195 ms: 1.32x faster                                                       |
| async_tree_memoization_tg  | 323 ms                                                 | 258 ms: 1.25x faster                                                       |
| raytrace                   | 212 ms                                                 | 170 ms: 1.25x faster                                                       |
| logging_silent             | 76.4 ns                                                | 63.2 ns: 1.21x faster                                                      |
| mako                       | 7.71 ms                                                | 6.39 ms: 1.21x faster                                                      |
| async_tree_io              | 668 ms                                                 | 555 ms: 1.20x faster                                                       |
| async_tree_io_tg           | 669 ms                                                 | 556 ms: 1.20x faster                                                       |
| comprehensions             | 14.5 us                                                | 12.1 us: 1.20x faster                                                      |
| coroutines                 | 19.2 ms                                                | 16.3 ms: 1.18x faster                                                      |
| deepcopy_memo              | 27.7 us                                                | 23.4 us: 1.18x faster                                                      |
| logging_simple             | 3.69 us                                                | 3.13 us: 1.18x faster                                                      |
| async_tree_memoization     | 312 ms                                                 | 267 ms: 1.17x faster                                                       |
| logging_format             | 3.98 us                                                | 3.41 us: 1.17x faster                                                      |
| unpickle_pure_python       | 151 us                                                 | 129 us: 1.17x faster                                                       |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 466 ms: 1.14x faster                                                       |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 460 ms: 1.14x faster                                                       |
| tomli_loads                | 1.39 sec                                               | 1.22 sec: 1.14x faster                                                     |
| float                      | 55.8 ms                                                | 49.4 ms: 1.13x faster                                                      |
| deepcopy_reduce            | 2.07 us                                                | 1.84 us: 1.13x faster                                                      |
| deltablue                  | 2.71 ms                                                | 2.41 ms: 1.12x faster                                                      |
| deepcopy                   | 235 us                                                 | 211 us: 1.11x faster                                                       |
| xml_etree_process          | 39.7 ms                                                | 35.7 ms: 1.11x faster                                                      |
| pprint_safe_repr           | 497 ms                                                 | 449 ms: 1.11x faster                                                       |
| pickle_pure_python         | 200 us                                                 | 181 us: 1.10x faster                                                       |
| richards                   | 32.1 ms                                                | 29.2 ms: 1.10x faster                                                      |
| pprint_pformat             | 1.01 sec                                               | 922 ms: 1.10x faster                                                       |
| richards_super             | 36.0 ms                                                | 32.9 ms: 1.09x faster                                                      |
| sqlglot_parse              | 848 us                                                 | 777 us: 1.09x faster                                                       |
| regex_compile              | 77.9 ms                                                | 71.5 ms: 1.09x faster                                                      |
| spectral_norm              | 76.4 ms                                                | 70.1 ms: 1.09x faster                                                      |
| nqueens                    | 62.4 ms                                                | 57.5 ms: 1.09x faster                                                      |
| sqlglot_transpile          | 1.02 ms                                                | 943 us: 1.08x faster                                                       |
| sympy_str                  | 148 ms                                                 | 137 ms: 1.08x faster                                                       |
| chaos                      | 42.5 ms                                                | 39.6 ms: 1.07x faster                                                      |
| sympy_sum                  | 77.6 ms                                                | 72.6 ms: 1.07x faster                                                      |
| sqlglot_normalize          | 186 ms                                                 | 174 ms: 1.07x faster                                                       |
| fannkuch                   | 248 ms                                                 | 233 ms: 1.07x faster                                                       |
| crypto_pyaes               | 51.9 ms                                                | 48.7 ms: 1.06x faster                                                      |
| chameleon                  | 4.70 ms                                                | 4.43 ms: 1.06x faster                                                      |
| xml_etree_iterparse        | 74.0 ms                                                | 69.9 ms: 1.06x faster                                                      |
| django_template            | 22.3 ms                                                | 21.2 ms: 1.06x faster                                                      |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 2.98 ms: 1.05x faster                                                      |
| json                       | 3.09 ms                                                | 2.94 ms: 1.05x faster                                                      |
| xml_etree_generate         | 55.8 ms                                                | 53.3 ms: 1.05x faster                                                      |
| pycparser                  | 677 ms                                                 | 646 ms: 1.05x faster                                                       |
| bench_thread_pool          | 504 us                                                 | 481 us: 1.05x faster                                                       |
| async_generators           | 304 ms                                                 | 291 ms: 1.04x faster                                                       |
| mdp                        | 1.58 sec                                               | 1.52 sec: 1.04x faster                                                     |
| hexiom                     | 4.54 ms                                                | 4.36 ms: 1.04x faster                                                      |
| sympy_integrate            | 11.4 ms                                                | 10.9 ms: 1.04x faster                                                      |
| pathlib                    | 24.2 ms                                                | 23.3 ms: 1.04x faster                                                      |
| unpickle_list              | 3.02 us                                                | 2.92 us: 1.04x faster                                                      |
| regex_dna                  | 154 ms                                                 | 149 ms: 1.03x faster                                                       |
| scimark_monte_carlo        | 45.0 ms                                                | 43.7 ms: 1.03x faster                                                      |
| dulwich_log                | 29.8 ms                                                | 29.0 ms: 1.03x faster                                                      |
| sqlglot_optimize           | 34.0 ms                                                | 33.1 ms: 1.03x faster                                                      |
| regex_effbot               | 2.64 ms                                                | 2.57 ms: 1.03x faster                                                      |
| sympy_expand               | 241 ms                                                 | 235 ms: 1.03x faster                                                       |
| xml_etree_parse            | 106 ms                                                 | 104 ms: 1.02x faster                                                       |
| scimark_fft                | 195 ms                                                 | 192 ms: 1.02x faster                                                       |
| nbody                      | 68.8 ms                                                | 67.8 ms: 1.02x faster                                                      |
| json_loads                 | 17.2 us                                                | 17.0 us: 1.02x faster                                                      |
| pyflate                    | 316 ms                                                 | 314 ms: 1.01x faster                                                       |
| pickle                     | 7.23 us                                                | 7.20 us: 1.00x faster                                                      |
| asyncio_websockets         | 409 ms                                                 | 408 ms: 1.00x faster                                                       |
| pidigits                   | 282 ms                                                 | 282 ms: 1.00x slower                                                       |
| pickle_dict                | 18.1 us                                                | 18.1 us: 1.00x slower                                                      |
| sqlite_synth               | 1.57 us                                                | 1.58 us: 1.00x slower                                                      |
| 2to3                       | 169 ms                                                 | 170 ms: 1.00x slower                                                       |
| unpickle                   | 9.12 us                                                | 9.21 us: 1.01x slower                                                      |
| meteor_contest             | 71.7 ms                                                | 72.5 ms: 1.01x slower                                                      |
| pickle_list                | 2.89 us                                                | 2.93 us: 1.01x slower                                                      |
| json_dumps                 | 6.22 ms                                                | 6.32 ms: 1.02x slower                                                      |
| gc_traversal               | 2.40 ms                                                | 2.46 ms: 1.02x slower                                                      |
| go                         | 102 ms                                                 | 105 ms: 1.04x slower                                                       |
| aiohttp                    | 1.08 ms                                                | 1.12 ms: 1.04x slower                                                      |
| scimark_lu                 | 76.0 ms                                                | 78.8 ms: 1.04x slower                                                      |
| bench_mp_pool              | 44.9 ms                                                | 46.7 ms: 1.04x slower                                                      |
| gunicorn                   | 1.15 ms                                                | 1.20 ms: 1.04x slower                                                      |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.33 sec: 1.07x slower                                                     |
| regex_v8                   | 16.0 ms                                                | 17.3 ms: 1.09x slower                                                      |
| typing_runtime_protocols   | 93.0 us                                                | 102 us: 1.09x slower                                                       |
| coverage                   | 38.9 ms                                                | 45.4 ms: 1.17x slower                                                      |
| scimark_sor                | 87.4 ms                                                | 103 ms: 1.18x slower                                                       |
| telco                      | 3.68 ms                                                | 4.45 ms: 1.21x slower                                                      |
| python_startup_no_site     | 9.37 ms                                                | 11.7 ms: 1.25x slower                                                      |
| python_startup             | 11.4 ms                                                | 14.5 ms: 1.27x slower                                                      |
| create_gc_cycles           | 701 us                                                 | 906 us: 1.29x slower                                                       |
| mypy2                      | 380 ms                                                 | 499 ms: 1.31x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                               |

Benchmark hidden because not significant (4): asyncio_tcp, docutils, dask, tornado_http
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240502-3.13.0a6+-6e8e3d5-JIT/bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.26x