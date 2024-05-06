# Results vs. 3.12.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: darwin-arm64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 165 ms: 1.03x faster                                                   |
| chameleon      | 4.70 ms                                                | 4.60 ms: 1.02x faster                                                  |
| docutils       | 1.50 sec                                               | 1.48 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 323 ms                                                 | 247 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 258 ms                                                 | 200 ms: 1.29x faster                                                   |
| async_tree_none            | 266 ms                                                 | 218 ms: 1.22x faster                                                   |
| async_tree_io              | 668 ms                                                 | 558 ms: 1.20x faster                                                   |
| async_tree_memoization     | 312 ms                                                 | 262 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 454 ms: 1.17x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 575 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 456 ms: 1.15x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 51.9 ms: 1.07x faster                                                  |
| nbody          | 68.8 ms                                                | 66.1 ms: 1.04x faster                                                  |
| pidigits       | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 77.9 ms                                                | 69.7 ms: 1.12x faster                                                  |
| regex_effbot   | 2.64 ms                                                | 2.59 ms: 1.02x faster                                                  |
| regex_dna      | 154 ms                                                 | 152 ms: 1.02x faster                                                   |
| regex_v8       | 16.0 ms                                                | 17.0 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 185 us: 1.08x faster                                                   |
| xml_etree_process    | 39.7 ms                                                | 37.8 ms: 1.05x faster                                                  |
| xml_etree_iterparse  | 74.0 ms                                                | 72.8 ms: 1.02x faster                                                  |
| xml_etree_generate   | 55.8 ms                                                | 55.2 ms: 1.01x faster                                                  |
| json_loads           | 17.2 us                                                | 17.1 us: 1.01x faster                                                  |
| unpickle_pure_python | 151 us                                                 | 150 us: 1.00x faster                                                   |
| pickle_dict          | 18.1 us                                                | 18.1 us: 1.00x slower                                                  |
| json_dumps           | 6.22 ms                                                | 6.25 ms: 1.00x slower                                                  |
| unpickle_list        | 3.02 us                                                | 3.04 us: 1.01x slower                                                  |
| unpickle             | 9.12 us                                                | 9.27 us: 1.02x slower                                                  |
| xml_etree_parse      | 106 ms                                                 | 109 ms: 1.02x slower                                                   |
| pickle               | 7.23 us                                                | 7.48 us: 1.03x slower                                                  |
| pickle_list          | 2.89 us                                                | 3.00 us: 1.04x slower                                                  |
| tomli_loads          | 1.39 sec                                               | 1.49 sec: 1.07x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.4 ms                                                | 11.9 ms: 1.05x slower                                                  |
| python_startup_no_site | 9.37 ms                                                | 10.2 ms: 1.09x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 7.71 ms                                                | 6.95 ms: 1.11x faster                                                  |
| django_template | 22.3 ms                                                | 20.7 ms: 1.08x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.09x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| comprehensions             | 14.5 us                                                | 10.2 us: 1.42x faster                                                  |
| raytrace                   | 212 ms                                                 | 157 ms: 1.35x faster                                                   |
| typing_runtime_protocols   | 93.0 us                                                | 70.8 us: 1.31x faster                                                  |
| async_tree_memoization_tg  | 323 ms                                                 | 247 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 258 ms                                                 | 200 ms: 1.29x faster                                                   |
| async_tree_none            | 266 ms                                                 | 218 ms: 1.22x faster                                                   |
| async_tree_io              | 668 ms                                                 | 558 ms: 1.20x faster                                                   |
| async_tree_memoization     | 312 ms                                                 | 262 ms: 1.19x faster                                                   |
| deltablue                  | 2.71 ms                                                | 2.30 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 454 ms: 1.17x faster                                                   |
| unpack_sequence            | 31.5 ns                                                | 26.9 ns: 1.17x faster                                                  |
| chaos                      | 42.5 ms                                                | 36.5 ms: 1.17x faster                                                  |
| async_tree_io_tg           | 669 ms                                                 | 575 ms: 1.16x faster                                                   |
| logging_silent             | 76.4 ns                                                | 65.9 ns: 1.16x faster                                                  |
| deepcopy_memo              | 27.7 us                                                | 23.9 us: 1.16x faster                                                  |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 456 ms: 1.15x faster                                                   |
| coroutines                 | 19.2 ms                                                | 17.0 ms: 1.13x faster                                                  |
| sqlglot_parse              | 848 us                                                 | 756 us: 1.12x faster                                                   |
| generators                 | 31.1 ms                                                | 27.7 ms: 1.12x faster                                                  |
| regex_compile              | 77.9 ms                                                | 69.7 ms: 1.12x faster                                                  |
| sympy_str                  | 148 ms                                                 | 132 ms: 1.11x faster                                                   |
| sqlglot_transpile          | 1.02 ms                                                | 918 us: 1.11x faster                                                   |
| nqueens                    | 62.4 ms                                                | 56.2 ms: 1.11x faster                                                  |
| mako                       | 7.71 ms                                                | 6.95 ms: 1.11x faster                                                  |
| sympy_sum                  | 77.6 ms                                                | 70.0 ms: 1.11x faster                                                  |
| logging_simple             | 3.69 us                                                | 3.34 us: 1.10x faster                                                  |
| scimark_lu                 | 76.0 ms                                                | 68.9 ms: 1.10x faster                                                  |
| crypto_pyaes               | 51.9 ms                                                | 47.2 ms: 1.10x faster                                                  |
| logging_format             | 3.98 us                                                | 3.62 us: 1.10x faster                                                  |
| sympy_integrate            | 11.4 ms                                                | 10.4 ms: 1.10x faster                                                  |
| deepcopy                   | 235 us                                                 | 215 us: 1.09x faster                                                   |
| deepcopy_reduce            | 2.07 us                                                | 1.91 us: 1.08x faster                                                  |
| pickle_pure_python         | 200 us                                                 | 185 us: 1.08x faster                                                   |
| django_template            | 22.3 ms                                                | 20.7 ms: 1.08x faster                                                  |
| sqlglot_normalize          | 186 ms                                                 | 172 ms: 1.08x faster                                                   |
| asyncio_tcp                | 449 ms                                                 | 417 ms: 1.08x faster                                                   |
| float                      | 55.8 ms                                                | 51.9 ms: 1.07x faster                                                  |
| spectral_norm              | 76.4 ms                                                | 71.3 ms: 1.07x faster                                                  |
| hexiom                     | 4.54 ms                                                | 4.27 ms: 1.06x faster                                                  |
| async_generators           | 304 ms                                                 | 286 ms: 1.06x faster                                                   |
| sqlglot_optimize           | 34.0 ms                                                | 32.1 ms: 1.06x faster                                                  |
| bench_thread_pool          | 504 us                                                 | 476 us: 1.06x faster                                                   |
| xml_etree_process          | 39.7 ms                                                | 37.8 ms: 1.05x faster                                                  |
| bench_mp_pool              | 44.9 ms                                                | 42.9 ms: 1.05x faster                                                  |
| gunicorn                   | 1.15 ms                                                | 1.10 ms: 1.04x faster                                                  |
| nbody                      | 68.8 ms                                                | 66.1 ms: 1.04x faster                                                  |
| json                       | 3.09 ms                                                | 2.97 ms: 1.04x faster                                                  |
| dulwich_log                | 29.8 ms                                                | 28.9 ms: 1.03x faster                                                  |
| richards_super             | 36.0 ms                                                | 34.9 ms: 1.03x faster                                                  |
| mdp                        | 1.58 sec                                               | 1.53 sec: 1.03x faster                                                 |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.05 ms: 1.03x faster                                                  |
| 2to3                       | 169 ms                                                 | 165 ms: 1.03x faster                                                   |
| richards                   | 32.1 ms                                                | 31.3 ms: 1.03x faster                                                  |
| pycparser                  | 677 ms                                                 | 660 ms: 1.03x faster                                                   |
| pprint_safe_repr           | 497 ms                                                 | 486 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.01 sec                                               | 989 ms: 1.02x faster                                                   |
| chameleon                  | 4.70 ms                                                | 4.60 ms: 1.02x faster                                                  |
| regex_effbot               | 2.64 ms                                                | 2.59 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 74.0 ms                                                | 72.8 ms: 1.02x faster                                                  |
| regex_dna                  | 154 ms                                                 | 152 ms: 1.02x faster                                                   |
| dask                       | 222 ms                                                 | 219 ms: 1.01x faster                                                   |
| docutils                   | 1.50 sec                                               | 1.48 sec: 1.01x faster                                                 |
| xml_etree_generate         | 55.8 ms                                                | 55.2 ms: 1.01x faster                                                  |
| go                         | 102 ms                                                 | 101 ms: 1.01x faster                                                   |
| scimark_monte_carlo        | 45.0 ms                                                | 44.6 ms: 1.01x faster                                                  |
| meteor_contest             | 71.7 ms                                                | 71.3 ms: 1.01x faster                                                  |
| json_loads                 | 17.2 us                                                | 17.1 us: 1.01x faster                                                  |
| unpickle_pure_python       | 151 us                                                 | 150 us: 1.00x faster                                                   |
| scimark_fft                | 195 ms                                                 | 195 ms: 1.00x faster                                                   |
| asyncio_websockets         | 409 ms                                                 | 408 ms: 1.00x faster                                                   |
| pickle_dict                | 18.1 us                                                | 18.1 us: 1.00x slower                                                  |
| pidigits                   | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| json_dumps                 | 6.22 ms                                                | 6.25 ms: 1.00x slower                                                  |
| unpickle_list              | 3.02 us                                                | 3.04 us: 1.01x slower                                                  |
| gc_traversal               | 2.40 ms                                                | 2.43 ms: 1.01x slower                                                  |
| pathlib                    | 24.2 ms                                                | 24.6 ms: 1.02x slower                                                  |
| unpickle                   | 9.12 us                                                | 9.27 us: 1.02x slower                                                  |
| xml_etree_parse            | 106 ms                                                 | 109 ms: 1.02x slower                                                   |
| pickle                     | 7.23 us                                                | 7.48 us: 1.03x slower                                                  |
| pickle_list                | 2.89 us                                                | 3.00 us: 1.04x slower                                                  |
| pyflate                    | 316 ms                                                 | 329 ms: 1.04x slower                                                   |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.30 sec: 1.04x slower                                                 |
| python_startup             | 11.4 ms                                                | 11.9 ms: 1.05x slower                                                  |
| fannkuch                   | 248 ms                                                 | 263 ms: 1.06x slower                                                   |
| regex_v8                   | 16.0 ms                                                | 17.0 ms: 1.06x slower                                                  |
| tomli_loads                | 1.39 sec                                               | 1.49 sec: 1.07x slower                                                 |
| python_startup_no_site     | 9.37 ms                                                | 10.2 ms: 1.09x slower                                                  |
| scimark_sor                | 87.4 ms                                                | 101 ms: 1.15x slower                                                   |
| create_gc_cycles           | 701 us                                                 | 835 us: 1.19x slower                                                   |
| coverage                   | 38.9 ms                                                | 46.8 ms: 1.20x slower                                                  |
| telco                      | 3.68 ms                                                | 4.54 ms: 1.23x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (5): aiohttp, sqlite_synth, mypy2, sympy_expand, tornado_http
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (13) of results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.04x