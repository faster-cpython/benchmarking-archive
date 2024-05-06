# Results vs. 3.12.0

- fork: python
- ref: 434bc593df4c0274b8af
- machine: darwin-arm64
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.03x faster
- HPT reliability: 98.91%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 172 ms: 1.01x slower                                                   |
| chameleon      | 4.70 ms                                                | 4.49 ms: 1.05x faster                                                  |
| docutils       | 1.50 sec                                               | 1.56 sec: 1.04x slower                                                 |
| tornado_http   | 69.3 ms                                                | 77.3 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 258 ms                                                 | 197 ms: 1.31x faster                                                   |
| async_tree_none            | 266 ms                                                 | 203 ms: 1.31x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 261 ms: 1.24x faster                                                   |
| async_tree_memoization     | 312 ms                                                 | 262 ms: 1.19x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 562 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 455 ms: 1.17x faster                                                   |
| async_tree_io              | 668 ms                                                 | 576 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 463 ms: 1.14x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 49.4 ms: 1.13x faster                                                  |
| pidigits       | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| nbody          | 68.8 ms                                                | 70.7 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 154 ms                                                 | 157 ms: 1.01x slower                                                   |
| regex_v8       | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                  |
| regex_effbot   | 2.64 ms                                                | 2.89 ms: 1.09x slower                                                  |
| regex_compile  | 77.9 ms                                                | 85.6 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 180 us: 1.11x faster                                                   |
| tomli_loads          | 1.39 sec                                               | 1.28 sec: 1.09x faster                                                 |
| unpickle_pure_python | 151 us                                                 | 141 us: 1.07x faster                                                   |
| xml_etree_process    | 39.7 ms                                                | 37.3 ms: 1.06x faster                                                  |
| xml_etree_generate   | 55.8 ms                                                | 54.7 ms: 1.02x faster                                                  |
| json_loads           | 17.2 us                                                | 16.9 us: 1.02x faster                                                  |
| xml_etree_iterparse  | 74.0 ms                                                | 72.9 ms: 1.02x faster                                                  |
| xml_etree_parse      | 106 ms                                                 | 107 ms: 1.01x slower                                                   |
| unpickle_list        | 3.02 us                                                | 3.05 us: 1.01x slower                                                  |
| json_dumps           | 6.22 ms                                                | 6.33 ms: 1.02x slower                                                  |
| pickle_list          | 2.89 us                                                | 2.97 us: 1.03x slower                                                  |
| pickle               | 7.23 us                                                | 7.45 us: 1.03x slower                                                  |
| unpickle             | 9.12 us                                                | 9.67 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.4 ms                                                | 13.3 ms: 1.17x slower                                                  |
| python_startup_no_site | 9.37 ms                                                | 11.6 ms: 1.24x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|-----------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako      | 7.71 ms                                                | 6.94 ms: 1.11x faster                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 93.0 us                                                | 69.1 us: 1.35x faster                                                  |
| async_tree_none_tg         | 258 ms                                                 | 197 ms: 1.31x faster                                                   |
| async_tree_none            | 266 ms                                                 | 203 ms: 1.31x faster                                                   |
| raytrace                   | 212 ms                                                 | 163 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 261 ms: 1.24x faster                                                   |
| comprehensions             | 14.5 us                                                | 12.0 us: 1.21x faster                                                  |
| async_tree_memoization     | 312 ms                                                 | 262 ms: 1.19x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 562 ms: 1.19x faster                                                   |
| generators                 | 31.1 ms                                                | 26.3 ms: 1.18x faster                                                  |
| logging_simple             | 3.69 us                                                | 3.12 us: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 455 ms: 1.17x faster                                                   |
| logging_silent             | 76.4 ns                                                | 65.4 ns: 1.17x faster                                                  |
| logging_format             | 3.98 us                                                | 3.43 us: 1.16x faster                                                  |
| async_tree_io              | 668 ms                                                 | 576 ms: 1.16x faster                                                   |
| deepcopy_memo              | 27.7 us                                                | 24.1 us: 1.15x faster                                                  |
| asyncio_tcp                | 449 ms                                                 | 394 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 463 ms: 1.14x faster                                                   |
| coroutines                 | 19.2 ms                                                | 17.0 ms: 1.13x faster                                                  |
| float                      | 55.8 ms                                                | 49.4 ms: 1.13x faster                                                  |
| crypto_pyaes               | 51.9 ms                                                | 46.5 ms: 1.11x faster                                                  |
| deepcopy_reduce            | 2.07 us                                                | 1.86 us: 1.11x faster                                                  |
| mako                       | 7.71 ms                                                | 6.94 ms: 1.11x faster                                                  |
| deepcopy                   | 235 us                                                 | 211 us: 1.11x faster                                                   |
| pickle_pure_python         | 200 us                                                 | 180 us: 1.11x faster                                                   |
| sqlglot_parse              | 848 us                                                 | 765 us: 1.11x faster                                                   |
| chaos                      | 42.5 ms                                                | 38.6 ms: 1.10x faster                                                  |
| richards                   | 32.1 ms                                                | 29.2 ms: 1.10x faster                                                  |
| richards_super             | 36.0 ms                                                | 32.9 ms: 1.10x faster                                                  |
| deltablue                  | 2.71 ms                                                | 2.48 ms: 1.09x faster                                                  |
| sqlglot_transpile          | 1.02 ms                                                | 939 us: 1.09x faster                                                   |
| tomli_loads                | 1.39 sec                                               | 1.28 sec: 1.09x faster                                                 |
| unpickle_pure_python       | 151 us                                                 | 141 us: 1.07x faster                                                   |
| xml_etree_process          | 39.7 ms                                                | 37.3 ms: 1.06x faster                                                  |
| sqlglot_normalize          | 186 ms                                                 | 176 ms: 1.05x faster                                                   |
| json                       | 3.09 ms                                                | 2.95 ms: 1.05x faster                                                  |
| chameleon                  | 4.70 ms                                                | 4.49 ms: 1.05x faster                                                  |
| sympy_str                  | 148 ms                                                 | 142 ms: 1.04x faster                                                   |
| bench_thread_pool          | 504 us                                                 | 486 us: 1.04x faster                                                   |
| spectral_norm              | 76.4 ms                                                | 73.7 ms: 1.04x faster                                                  |
| pycparser                  | 677 ms                                                 | 654 ms: 1.03x faster                                                   |
| nqueens                    | 62.4 ms                                                | 60.4 ms: 1.03x faster                                                  |
| scimark_monte_carlo        | 45.0 ms                                                | 43.8 ms: 1.03x faster                                                  |
| dulwich_log                | 29.8 ms                                                | 29.0 ms: 1.03x faster                                                  |
| xml_etree_generate         | 55.8 ms                                                | 54.7 ms: 1.02x faster                                                  |
| json_loads                 | 17.2 us                                                | 16.9 us: 1.02x faster                                                  |
| async_generators           | 304 ms                                                 | 299 ms: 1.02x faster                                                   |
| sympy_expand               | 241 ms                                                 | 237 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 74.0 ms                                                | 72.9 ms: 1.02x faster                                                  |
| sympy_sum                  | 77.6 ms                                                | 76.6 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 497 ms                                                 | 492 ms: 1.01x faster                                                   |
| sqlglot_optimize           | 34.0 ms                                                | 33.7 ms: 1.01x faster                                                  |
| pprint_pformat             | 1.01 sec                                               | 1.00 sec: 1.01x faster                                                 |
| pyflate                    | 316 ms                                                 | 316 ms: 1.00x slower                                                   |
| pidigits                   | 282 ms                                                 | 283 ms: 1.00x slower                                                   |
| xml_etree_parse            | 106 ms                                                 | 107 ms: 1.01x slower                                                   |
| unpickle_list              | 3.02 us                                                | 3.05 us: 1.01x slower                                                  |
| sqlite_synth               | 1.57 us                                                | 1.59 us: 1.01x slower                                                  |
| 2to3                       | 169 ms                                                 | 172 ms: 1.01x slower                                                   |
| regex_dna                  | 154 ms                                                 | 157 ms: 1.01x slower                                                   |
| json_dumps                 | 6.22 ms                                                | 6.33 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.20 ms: 1.02x slower                                                  |
| meteor_contest             | 71.7 ms                                                | 73.4 ms: 1.02x slower                                                  |
| gc_traversal               | 2.40 ms                                                | 2.46 ms: 1.02x slower                                                  |
| nbody                      | 68.8 ms                                                | 70.7 ms: 1.03x slower                                                  |
| scimark_fft                | 195 ms                                                 | 200 ms: 1.03x slower                                                   |
| pathlib                    | 24.2 ms                                                | 24.9 ms: 1.03x slower                                                  |
| pickle_list                | 2.89 us                                                | 2.97 us: 1.03x slower                                                  |
| bench_mp_pool              | 44.9 ms                                                | 46.3 ms: 1.03x slower                                                  |
| pickle                     | 7.23 us                                                | 7.45 us: 1.03x slower                                                  |
| docutils                   | 1.50 sec                                               | 1.56 sec: 1.04x slower                                                 |
| go                         | 102 ms                                                 | 106 ms: 1.05x slower                                                   |
| fannkuch                   | 248 ms                                                 | 261 ms: 1.05x slower                                                   |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.31 sec: 1.05x slower                                                 |
| hexiom                     | 4.54 ms                                                | 4.81 ms: 1.06x slower                                                  |
| unpickle                   | 9.12 us                                                | 9.67 us: 1.06x slower                                                  |
| mypy2                      | 380 ms                                                 | 409 ms: 1.08x slower                                                   |
| scimark_lu                 | 76.0 ms                                                | 82.7 ms: 1.09x slower                                                  |
| regex_v8                   | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                  |
| regex_effbot               | 2.64 ms                                                | 2.89 ms: 1.09x slower                                                  |
| regex_compile              | 77.9 ms                                                | 85.6 ms: 1.10x slower                                                  |
| tornado_http               | 69.3 ms                                                | 77.3 ms: 1.12x slower                                                  |
| python_startup             | 11.4 ms                                                | 13.3 ms: 1.17x slower                                                  |
| coverage                   | 38.9 ms                                                | 46.9 ms: 1.21x slower                                                  |
| scimark_sor                | 87.4 ms                                                | 106 ms: 1.21x slower                                                   |
| python_startup_no_site     | 9.37 ms                                                | 11.6 ms: 1.24x slower                                                  |
| telco                      | 3.68 ms                                                | 4.65 ms: 1.26x slower                                                  |
| create_gc_cycles           | 701 us                                                 | 901 us: 1.29x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (7): aiohttp, dask, asyncio_websockets, mdp, pickle_dict, sympy_integrate, gunicorn
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240404-3.13.0a5+-434bc59-JIT/bm-20240404-darwin-arm64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 98.91% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.24x