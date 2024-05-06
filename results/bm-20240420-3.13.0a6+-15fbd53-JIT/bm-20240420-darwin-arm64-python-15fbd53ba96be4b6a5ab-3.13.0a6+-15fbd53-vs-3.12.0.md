# Results vs. 3.12.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: darwin-arm64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 168 ms: 1.01x faster                                                   |
| chameleon      | 4.70 ms                                                | 4.47 ms: 1.05x faster                                                  |
| docutils       | 1.50 sec                                               | 1.49 sec: 1.00x faster                                                 |
| tornado_http   | 69.3 ms                                                | 76.6 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 266 ms                                                 | 201 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 258 ms                                                 | 195 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 259 ms: 1.25x faster                                                   |
| async_tree_io_tg           | 669 ms                                                 | 553 ms: 1.21x faster                                                   |
| async_tree_io              | 668 ms                                                 | 557 ms: 1.20x faster                                                   |
| async_tree_memoization     | 312 ms                                                 | 268 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 465 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 460 ms: 1.14x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 48.6 ms: 1.15x faster                                                  |
| pidigits       | 282 ms                                                 | 282 ms: 1.00x slower                                                   |
| nbody          | 68.8 ms                                                | 70.1 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 154 ms                                                 | 149 ms: 1.03x faster                                                   |
| regex_effbot   | 2.64 ms                                                | 2.57 ms: 1.03x faster                                                  |
| regex_compile  | 77.9 ms                                                | 83.3 ms: 1.07x slower                                                  |
| regex_v8       | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 180 us: 1.11x faster                                                   |
| unpickle_pure_python | 151 us                                                 | 135 us: 1.11x faster                                                   |
| tomli_loads          | 1.39 sec                                               | 1.26 sec: 1.10x faster                                                 |
| xml_etree_iterparse  | 74.0 ms                                                | 67.7 ms: 1.09x faster                                                  |
| xml_etree_parse      | 106 ms                                                 | 97.8 ms: 1.09x faster                                                  |
| xml_etree_process    | 39.7 ms                                                | 36.7 ms: 1.08x faster                                                  |
| xml_etree_generate   | 55.8 ms                                                | 52.8 ms: 1.06x faster                                                  |
| unpickle_list        | 3.02 us                                                | 2.93 us: 1.03x faster                                                  |
| json_loads           | 17.2 us                                                | 17.0 us: 1.01x faster                                                  |
| pickle_dict          | 18.1 us                                                | 18.1 us: 1.00x slower                                                  |
| unpickle             | 9.12 us                                                | 9.18 us: 1.01x slower                                                  |
| json_dumps           | 6.22 ms                                                | 6.35 ms: 1.02x slower                                                  |
| pickle               | 7.23 us                                                | 7.43 us: 1.03x slower                                                  |
| pickle_list          | 2.89 us                                                | 3.01 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 9.37 ms                                                | 10.5 ms: 1.12x slower                                                  |
| python_startup         | 11.4 ms                                                | 13.3 ms: 1.17x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 7.71 ms                                                | 6.87 ms: 1.12x faster                                                  |
| django_template | 22.3 ms                                                | 20.4 ms: 1.09x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.11x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 93.0 us                                                | 68.1 us: 1.37x faster                                                  |
| async_tree_none            | 266 ms                                                 | 201 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 258 ms                                                 | 195 ms: 1.32x faster                                                   |
| raytrace                   | 212 ms                                                 | 163 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 323 ms                                                 | 259 ms: 1.25x faster                                                   |
| comprehensions             | 14.5 us                                                | 11.8 us: 1.23x faster                                                  |
| async_tree_io_tg           | 669 ms                                                 | 553 ms: 1.21x faster                                                   |
| logging_silent             | 76.4 ns                                                | 63.5 ns: 1.20x faster                                                  |
| logging_simple             | 3.69 us                                                | 3.07 us: 1.20x faster                                                  |
| async_tree_io              | 668 ms                                                 | 557 ms: 1.20x faster                                                   |
| logging_format             | 3.98 us                                                | 3.34 us: 1.19x faster                                                  |
| generators                 | 31.1 ms                                                | 26.4 ms: 1.18x faster                                                  |
| async_tree_memoization     | 312 ms                                                 | 268 ms: 1.17x faster                                                   |
| deepcopy_memo              | 27.7 us                                                | 24.1 us: 1.15x faster                                                  |
| float                      | 55.8 ms                                                | 48.6 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 465 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 460 ms: 1.14x faster                                                   |
| mako                       | 7.71 ms                                                | 6.87 ms: 1.12x faster                                                  |
| deepcopy_reduce            | 2.07 us                                                | 1.84 us: 1.12x faster                                                  |
| chaos                      | 42.5 ms                                                | 37.9 ms: 1.12x faster                                                  |
| crypto_pyaes               | 51.9 ms                                                | 46.2 ms: 1.12x faster                                                  |
| sqlglot_parse              | 848 us                                                 | 758 us: 1.12x faster                                                   |
| coroutines                 | 19.2 ms                                                | 17.2 ms: 1.12x faster                                                  |
| pickle_pure_python         | 200 us                                                 | 180 us: 1.11x faster                                                   |
| unpickle_pure_python       | 151 us                                                 | 135 us: 1.11x faster                                                   |
| deepcopy                   | 235 us                                                 | 212 us: 1.11x faster                                                   |
| tomli_loads                | 1.39 sec                                               | 1.26 sec: 1.10x faster                                                 |
| asyncio_tcp                | 449 ms                                                 | 407 ms: 1.10x faster                                                   |
| richards_super             | 36.0 ms                                                | 32.8 ms: 1.10x faster                                                  |
| sqlglot_transpile          | 1.02 ms                                                | 929 us: 1.10x faster                                                   |
| deltablue                  | 2.71 ms                                                | 2.47 ms: 1.10x faster                                                  |
| xml_etree_iterparse        | 74.0 ms                                                | 67.7 ms: 1.09x faster                                                  |
| django_template            | 22.3 ms                                                | 20.4 ms: 1.09x faster                                                  |
| richards                   | 32.1 ms                                                | 29.5 ms: 1.09x faster                                                  |
| xml_etree_parse            | 106 ms                                                 | 97.8 ms: 1.09x faster                                                  |
| xml_etree_process          | 39.7 ms                                                | 36.7 ms: 1.08x faster                                                  |
| sqlglot_normalize          | 186 ms                                                 | 173 ms: 1.07x faster                                                   |
| sympy_str                  | 148 ms                                                 | 139 ms: 1.06x faster                                                   |
| json                       | 3.09 ms                                                | 2.91 ms: 1.06x faster                                                  |
| xml_etree_generate         | 55.8 ms                                                | 52.8 ms: 1.06x faster                                                  |
| nqueens                    | 62.4 ms                                                | 59.3 ms: 1.05x faster                                                  |
| chameleon                  | 4.70 ms                                                | 4.47 ms: 1.05x faster                                                  |
| dulwich_log                | 29.8 ms                                                | 28.4 ms: 1.05x faster                                                  |
| pycparser                  | 677 ms                                                 | 645 ms: 1.05x faster                                                   |
| scimark_monte_carlo        | 45.0 ms                                                | 43.0 ms: 1.05x faster                                                  |
| sympy_sum                  | 77.6 ms                                                | 74.8 ms: 1.04x faster                                                  |
| spectral_norm              | 76.4 ms                                                | 73.7 ms: 1.04x faster                                                  |
| regex_dna                  | 154 ms                                                 | 149 ms: 1.03x faster                                                   |
| bench_thread_pool          | 504 us                                                 | 487 us: 1.03x faster                                                   |
| sympy_expand               | 241 ms                                                 | 234 ms: 1.03x faster                                                   |
| unpickle_list              | 3.02 us                                                | 2.93 us: 1.03x faster                                                  |
| pathlib                    | 24.2 ms                                                | 23.5 ms: 1.03x faster                                                  |
| sqlglot_optimize           | 34.0 ms                                                | 33.1 ms: 1.03x faster                                                  |
| async_generators           | 304 ms                                                 | 296 ms: 1.03x faster                                                   |
| regex_effbot               | 2.64 ms                                                | 2.57 ms: 1.03x faster                                                  |
| pprint_safe_repr           | 497 ms                                                 | 486 ms: 1.02x faster                                                   |
| sympy_integrate            | 11.4 ms                                                | 11.2 ms: 1.02x faster                                                  |
| pprint_pformat             | 1.01 sec                                               | 995 ms: 1.02x faster                                                   |
| json_loads                 | 17.2 us                                                | 17.0 us: 1.01x faster                                                  |
| mdp                        | 1.58 sec                                               | 1.57 sec: 1.01x faster                                                 |
| 2to3                       | 169 ms                                                 | 168 ms: 1.01x faster                                                   |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.12 ms: 1.01x faster                                                  |
| pyflate                    | 316 ms                                                 | 314 ms: 1.00x faster                                                   |
| docutils                   | 1.50 sec                                               | 1.49 sec: 1.00x faster                                                 |
| asyncio_websockets         | 409 ms                                                 | 409 ms: 1.00x faster                                                   |
| sqlite_synth               | 1.57 us                                                | 1.57 us: 1.00x slower                                                  |
| pidigits                   | 282 ms                                                 | 282 ms: 1.00x slower                                                   |
| pickle_dict                | 18.1 us                                                | 18.1 us: 1.00x slower                                                  |
| unpickle                   | 9.12 us                                                | 9.18 us: 1.01x slower                                                  |
| nbody                      | 68.8 ms                                                | 70.1 ms: 1.02x slower                                                  |
| meteor_contest             | 71.7 ms                                                | 73.1 ms: 1.02x slower                                                  |
| gc_traversal               | 2.40 ms                                                | 2.45 ms: 1.02x slower                                                  |
| json_dumps                 | 6.22 ms                                                | 6.35 ms: 1.02x slower                                                  |
| scimark_fft                | 195 ms                                                 | 201 ms: 1.03x slower                                                   |
| pickle                     | 7.23 us                                                | 7.43 us: 1.03x slower                                                  |
| bench_mp_pool              | 44.9 ms                                                | 46.2 ms: 1.03x slower                                                  |
| hexiom                     | 4.54 ms                                                | 4.71 ms: 1.04x slower                                                  |
| fannkuch                   | 248 ms                                                 | 258 ms: 1.04x slower                                                   |
| gunicorn                   | 1.15 ms                                                | 1.19 ms: 1.04x slower                                                  |
| aiohttp                    | 1.08 ms                                                | 1.12 ms: 1.04x slower                                                  |
| pickle_list                | 2.89 us                                                | 3.01 us: 1.04x slower                                                  |
| go                         | 102 ms                                                 | 106 ms: 1.04x slower                                                   |
| mypy2                      | 380 ms                                                 | 402 ms: 1.06x slower                                                   |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.32 sec: 1.06x slower                                                 |
| regex_compile              | 77.9 ms                                                | 83.3 ms: 1.07x slower                                                  |
| scimark_lu                 | 76.0 ms                                                | 81.6 ms: 1.07x slower                                                  |
| regex_v8                   | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                  |
| tornado_http               | 69.3 ms                                                | 76.6 ms: 1.11x slower                                                  |
| python_startup_no_site     | 9.37 ms                                                | 10.5 ms: 1.12x slower                                                  |
| python_startup             | 11.4 ms                                                | 13.3 ms: 1.17x slower                                                  |
| coverage                   | 38.9 ms                                                | 46.4 ms: 1.19x slower                                                  |
| scimark_sor                | 87.4 ms                                                | 105 ms: 1.20x slower                                                   |
| create_gc_cycles           | 701 us                                                 | 872 us: 1.24x slower                                                   |
| telco                      | 3.68 ms                                                | 4.58 ms: 1.24x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (1): dask
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.25x