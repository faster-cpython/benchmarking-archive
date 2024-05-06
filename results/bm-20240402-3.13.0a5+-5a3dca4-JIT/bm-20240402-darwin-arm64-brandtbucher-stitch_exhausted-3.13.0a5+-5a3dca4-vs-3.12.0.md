# Results vs. 3.12.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: darwin-arm64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.01x faster
- HPT reliability: 86.83%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.28x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 176 ms: 1.04x slower                                                     |
| chameleon      | 4.70 ms                                                | 4.47 ms: 1.05x faster                                                    |
| docutils       | 1.50 sec                                               | 1.58 sec: 1.05x slower                                                   |
| tornado_http   | 69.3 ms                                                | 82.2 ms: 1.19x slower                                                    |
| Geometric mean | (ref)                                                  | 1.05x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 323 ms                                                 | 249 ms: 1.29x faster                                                     |
| async_tree_none_tg         | 258 ms                                                 | 201 ms: 1.28x faster                                                     |
| async_tree_io_tg           | 669 ms                                                 | 557 ms: 1.20x faster                                                     |
| async_tree_memoization     | 312 ms                                                 | 266 ms: 1.17x faster                                                     |
| async_tree_io              | 668 ms                                                 | 569 ms: 1.17x faster                                                     |
| async_tree_none            | 266 ms                                                 | 228 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 462 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 466 ms: 1.13x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 49.2 ms: 1.13x faster                                                    |
| pidigits       | 282 ms                                                 | 283 ms: 1.00x slower                                                     |
| nbody          | 68.8 ms                                                | 70.0 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 154 ms                                                 | 152 ms: 1.01x faster                                                     |
| regex_effbot   | 2.64 ms                                                | 2.62 ms: 1.01x faster                                                    |
| regex_v8       | 16.0 ms                                                | 17.1 ms: 1.07x slower                                                    |
| regex_compile  | 77.9 ms                                                | 87.2 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 183 us: 1.10x faster                                                     |
| xml_etree_process    | 39.7 ms                                                | 36.5 ms: 1.09x faster                                                    |
| tomli_loads          | 1.39 sec                                               | 1.29 sec: 1.08x faster                                                   |
| xml_etree_iterparse  | 74.0 ms                                                | 68.5 ms: 1.08x faster                                                    |
| xml_etree_parse      | 106 ms                                                 | 98.3 ms: 1.08x faster                                                    |
| unpickle_pure_python | 151 us                                                 | 143 us: 1.05x faster                                                     |
| xml_etree_generate   | 55.8 ms                                                | 54.1 ms: 1.03x faster                                                    |
| json_loads           | 17.2 us                                                | 17.1 us: 1.01x faster                                                    |
| unpickle             | 9.12 us                                                | 9.17 us: 1.01x slower                                                    |
| unpickle_list        | 3.02 us                                                | 3.04 us: 1.01x slower                                                    |
| json_dumps           | 6.22 ms                                                | 6.28 ms: 1.01x slower                                                    |
| pickle_list          | 2.89 us                                                | 2.98 us: 1.03x slower                                                    |
| pickle               | 7.23 us                                                | 7.47 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                             |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 11.4 ms                                                | 13.4 ms: 1.17x slower                                                    |
| python_startup_no_site | 9.37 ms                                                | 11.6 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 7.71 ms                                                | 6.96 ms: 1.11x faster                                                    |
| django_template | 22.3 ms                                                | 21.3 ms: 1.05x faster                                                    |
| Geometric mean  | (ref)                                                  | 1.08x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 93.0 us                                                | 69.9 us: 1.33x faster                                                    |
| async_tree_memoization_tg  | 323 ms                                                 | 249 ms: 1.29x faster                                                     |
| async_tree_none_tg         | 258 ms                                                 | 201 ms: 1.28x faster                                                     |
| async_tree_io_tg           | 669 ms                                                 | 557 ms: 1.20x faster                                                     |
| comprehensions             | 14.5 us                                                | 12.1 us: 1.20x faster                                                    |
| generators                 | 31.1 ms                                                | 26.2 ms: 1.19x faster                                                    |
| async_tree_memoization     | 312 ms                                                 | 266 ms: 1.17x faster                                                     |
| async_tree_io              | 668 ms                                                 | 569 ms: 1.17x faster                                                     |
| raytrace                   | 212 ms                                                 | 181 ms: 1.17x faster                                                     |
| async_tree_none            | 266 ms                                                 | 228 ms: 1.17x faster                                                     |
| logging_silent             | 76.4 ns                                                | 65.7 ns: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 462 ms: 1.15x faster                                                     |
| coroutines                 | 19.2 ms                                                | 16.7 ms: 1.15x faster                                                    |
| deltablue                  | 2.71 ms                                                | 2.37 ms: 1.14x faster                                                    |
| deepcopy_memo              | 27.7 us                                                | 24.3 us: 1.14x faster                                                    |
| float                      | 55.8 ms                                                | 49.2 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 466 ms: 1.13x faster                                                     |
| logging_simple             | 3.69 us                                                | 3.29 us: 1.12x faster                                                    |
| logging_format             | 3.98 us                                                | 3.59 us: 1.11x faster                                                    |
| mako                       | 7.71 ms                                                | 6.96 ms: 1.11x faster                                                    |
| deepcopy_reduce            | 2.07 us                                                | 1.87 us: 1.11x faster                                                    |
| sqlglot_parse              | 848 us                                                 | 769 us: 1.10x faster                                                     |
| pickle_pure_python         | 200 us                                                 | 183 us: 1.10x faster                                                     |
| crypto_pyaes               | 51.9 ms                                                | 47.5 ms: 1.09x faster                                                    |
| deepcopy                   | 235 us                                                 | 215 us: 1.09x faster                                                     |
| xml_etree_process          | 39.7 ms                                                | 36.5 ms: 1.09x faster                                                    |
| tomli_loads                | 1.39 sec                                               | 1.29 sec: 1.08x faster                                                   |
| sqlglot_transpile          | 1.02 ms                                                | 944 us: 1.08x faster                                                     |
| xml_etree_iterparse        | 74.0 ms                                                | 68.5 ms: 1.08x faster                                                    |
| xml_etree_parse            | 106 ms                                                 | 98.3 ms: 1.08x faster                                                    |
| chaos                      | 42.5 ms                                                | 39.4 ms: 1.08x faster                                                    |
| unpickle_pure_python       | 151 us                                                 | 143 us: 1.05x faster                                                     |
| chameleon                  | 4.70 ms                                                | 4.47 ms: 1.05x faster                                                    |
| django_template            | 22.3 ms                                                | 21.3 ms: 1.05x faster                                                    |
| json                       | 3.09 ms                                                | 2.95 ms: 1.05x faster                                                    |
| sqlglot_normalize          | 186 ms                                                 | 178 ms: 1.04x faster                                                     |
| spectral_norm              | 76.4 ms                                                | 73.8 ms: 1.04x faster                                                    |
| richards_super             | 36.0 ms                                                | 34.8 ms: 1.04x faster                                                    |
| sympy_str                  | 148 ms                                                 | 143 ms: 1.03x faster                                                     |
| xml_etree_generate         | 55.8 ms                                                | 54.1 ms: 1.03x faster                                                    |
| richards                   | 32.1 ms                                                | 31.2 ms: 1.03x faster                                                    |
| pycparser                  | 677 ms                                                 | 667 ms: 1.01x faster                                                     |
| regex_dna                  | 154 ms                                                 | 152 ms: 1.01x faster                                                     |
| nqueens                    | 62.4 ms                                                | 61.6 ms: 1.01x faster                                                    |
| async_generators           | 304 ms                                                 | 301 ms: 1.01x faster                                                     |
| json_loads                 | 17.2 us                                                | 17.1 us: 1.01x faster                                                    |
| regex_effbot               | 2.64 ms                                                | 2.62 ms: 1.01x faster                                                    |
| bench_thread_pool          | 504 us                                                 | 501 us: 1.01x faster                                                     |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.13 ms: 1.00x faster                                                    |
| asyncio_websockets         | 409 ms                                                 | 409 ms: 1.00x faster                                                     |
| pidigits                   | 282 ms                                                 | 283 ms: 1.00x slower                                                     |
| unpickle                   | 9.12 us                                                | 9.17 us: 1.01x slower                                                    |
| sqlite_synth               | 1.57 us                                                | 1.58 us: 1.01x slower                                                    |
| unpickle_list              | 3.02 us                                                | 3.04 us: 1.01x slower                                                    |
| json_dumps                 | 6.22 ms                                                | 6.28 ms: 1.01x slower                                                    |
| sqlglot_optimize           | 34.0 ms                                                | 34.4 ms: 1.01x slower                                                    |
| dulwich_log                | 29.8 ms                                                | 30.2 ms: 1.01x slower                                                    |
| dask                       | 222 ms                                                 | 226 ms: 1.02x slower                                                     |
| nbody                      | 68.8 ms                                                | 70.0 ms: 1.02x slower                                                    |
| scimark_monte_carlo        | 45.0 ms                                                | 45.9 ms: 1.02x slower                                                    |
| gc_traversal               | 2.40 ms                                                | 2.45 ms: 1.02x slower                                                    |
| pathlib                    | 24.2 ms                                                | 24.7 ms: 1.02x slower                                                    |
| scimark_fft                | 195 ms                                                 | 200 ms: 1.02x slower                                                     |
| sympy_integrate            | 11.4 ms                                                | 11.7 ms: 1.03x slower                                                    |
| pickle_list                | 2.89 us                                                | 2.98 us: 1.03x slower                                                    |
| pickle                     | 7.23 us                                                | 7.47 us: 1.03x slower                                                    |
| 2to3                       | 169 ms                                                 | 176 ms: 1.04x slower                                                     |
| meteor_contest             | 71.7 ms                                                | 74.4 ms: 1.04x slower                                                    |
| fannkuch                   | 248 ms                                                 | 258 ms: 1.04x slower                                                     |
| bench_mp_pool              | 44.9 ms                                                | 47.0 ms: 1.05x slower                                                    |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.30 sec: 1.05x slower                                                   |
| gunicorn                   | 1.15 ms                                                | 1.21 ms: 1.05x slower                                                    |
| docutils                   | 1.50 sec                                               | 1.58 sec: 1.05x slower                                                   |
| go                         | 102 ms                                                 | 107 ms: 1.06x slower                                                     |
| aiohttp                    | 1.08 ms                                                | 1.14 ms: 1.06x slower                                                    |
| pprint_pformat             | 1.01 sec                                               | 1.07 sec: 1.06x slower                                                   |
| pprint_safe_repr           | 497 ms                                                 | 527 ms: 1.06x slower                                                     |
| pyflate                    | 316 ms                                                 | 335 ms: 1.06x slower                                                     |
| scimark_lu                 | 76.0 ms                                                | 81.5 ms: 1.07x slower                                                    |
| regex_v8                   | 16.0 ms                                                | 17.1 ms: 1.07x slower                                                    |
| regex_compile              | 77.9 ms                                                | 87.2 ms: 1.12x slower                                                    |
| mypy2                      | 380 ms                                                 | 426 ms: 1.12x slower                                                     |
| hexiom                     | 4.54 ms                                                | 5.28 ms: 1.16x slower                                                    |
| python_startup             | 11.4 ms                                                | 13.4 ms: 1.17x slower                                                    |
| tornado_http               | 69.3 ms                                                | 82.2 ms: 1.19x slower                                                    |
| coverage                   | 38.9 ms                                                | 46.4 ms: 1.19x slower                                                    |
| create_gc_cycles           | 701 us                                                 | 847 us: 1.21x slower                                                     |
| telco                      | 3.68 ms                                                | 4.48 ms: 1.22x slower                                                    |
| scimark_sor                | 87.4 ms                                                | 108 ms: 1.23x slower                                                     |
| python_startup_no_site     | 9.37 ms                                                | 11.6 ms: 1.24x slower                                                    |
| unpack_sequence            | 31.5 ns                                                | 116 ns: 3.69x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (5): mdp, pickle_dict, sympy_expand, asyncio_tcp, sympy_sum
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (13) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 86.83% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.28x