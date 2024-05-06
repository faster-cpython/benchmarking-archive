# Results vs. 3.12.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: darwin-arm64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.03x faster
- HPT reliability: 93.16%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 173 ms: 1.02x slower                                                     |
| chameleon      | 4.70 ms                                                | 4.46 ms: 1.05x faster                                                    |
| docutils       | 1.50 sec                                               | 1.58 sec: 1.05x slower                                                   |
| tornado_http   | 69.3 ms                                                | 79.8 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none_tg         | 258 ms                                                 | 198 ms: 1.30x faster                                                     |
| async_tree_none            | 266 ms                                                 | 204 ms: 1.30x faster                                                     |
| async_tree_memoization_tg  | 323 ms                                                 | 261 ms: 1.24x faster                                                     |
| async_tree_io_tg           | 669 ms                                                 | 561 ms: 1.19x faster                                                     |
| async_tree_memoization     | 312 ms                                                 | 262 ms: 1.19x faster                                                     |
| async_tree_io              | 668 ms                                                 | 568 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 467 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 464 ms: 1.13x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 49.5 ms: 1.13x faster                                                    |
| pidigits       | 282 ms                                                 | 282 ms: 1.00x slower                                                     |
| nbody          | 68.8 ms                                                | 70.3 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                  | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 154 ms                                                 | 145 ms: 1.06x faster                                                     |
| regex_effbot   | 2.64 ms                                                | 2.56 ms: 1.03x faster                                                    |
| regex_v8       | 16.0 ms                                                | 17.2 ms: 1.08x slower                                                    |
| regex_compile  | 77.9 ms                                                | 86.1 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                  | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 183 us: 1.09x faster                                                     |
| xml_etree_process    | 39.7 ms                                                | 36.5 ms: 1.09x faster                                                    |
| tomli_loads          | 1.39 sec                                               | 1.29 sec: 1.08x faster                                                   |
| unpickle_pure_python | 151 us                                                 | 140 us: 1.08x faster                                                     |
| xml_etree_generate   | 55.8 ms                                                | 54.3 ms: 1.03x faster                                                    |
| xml_etree_iterparse  | 74.0 ms                                                | 72.2 ms: 1.03x faster                                                    |
| json_loads           | 17.2 us                                                | 17.1 us: 1.01x faster                                                    |
| pickle_dict          | 18.1 us                                                | 18.1 us: 1.00x slower                                                    |
| unpickle             | 9.12 us                                                | 9.27 us: 1.02x slower                                                    |
| json_dumps           | 6.22 ms                                                | 6.37 ms: 1.02x slower                                                    |
| pickle               | 7.23 us                                                | 7.49 us: 1.04x slower                                                    |
| pickle_list          | 2.89 us                                                | 3.00 us: 1.04x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_parse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 11.4 ms                                                | 13.5 ms: 1.18x slower                                                    |
| python_startup_no_site | 9.37 ms                                                | 11.7 ms: 1.25x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|-----------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako      | 7.71 ms                                                | 6.92 ms: 1.11x faster                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 93.0 us                                                | 70.3 us: 1.32x faster                                                    |
| async_tree_none_tg         | 258 ms                                                 | 198 ms: 1.30x faster                                                     |
| async_tree_none            | 266 ms                                                 | 204 ms: 1.30x faster                                                     |
| raytrace                   | 212 ms                                                 | 165 ms: 1.28x faster                                                     |
| async_tree_memoization_tg  | 323 ms                                                 | 261 ms: 1.24x faster                                                     |
| logging_silent             | 76.4 ns                                                | 63.8 ns: 1.20x faster                                                    |
| comprehensions             | 14.5 us                                                | 12.2 us: 1.20x faster                                                    |
| async_tree_io_tg           | 669 ms                                                 | 561 ms: 1.19x faster                                                     |
| async_tree_memoization     | 312 ms                                                 | 262 ms: 1.19x faster                                                     |
| generators                 | 31.1 ms                                                | 26.1 ms: 1.19x faster                                                    |
| async_tree_io              | 668 ms                                                 | 568 ms: 1.18x faster                                                     |
| logging_simple             | 3.69 us                                                | 3.17 us: 1.16x faster                                                    |
| logging_format             | 3.98 us                                                | 3.46 us: 1.15x faster                                                    |
| deepcopy_memo              | 27.7 us                                                | 24.2 us: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 467 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 464 ms: 1.13x faster                                                     |
| coroutines                 | 19.2 ms                                                | 17.0 ms: 1.13x faster                                                    |
| float                      | 55.8 ms                                                | 49.5 ms: 1.13x faster                                                    |
| deepcopy                   | 235 us                                                 | 211 us: 1.12x faster                                                     |
| mako                       | 7.71 ms                                                | 6.92 ms: 1.11x faster                                                    |
| deepcopy_reduce            | 2.07 us                                                | 1.86 us: 1.11x faster                                                    |
| crypto_pyaes               | 51.9 ms                                                | 46.9 ms: 1.11x faster                                                    |
| richards                   | 32.1 ms                                                | 29.1 ms: 1.11x faster                                                    |
| richards_super             | 36.0 ms                                                | 32.7 ms: 1.10x faster                                                    |
| sqlglot_parse              | 848 us                                                 | 772 us: 1.10x faster                                                     |
| chaos                      | 42.5 ms                                                | 38.9 ms: 1.09x faster                                                    |
| deltablue                  | 2.71 ms                                                | 2.48 ms: 1.09x faster                                                    |
| pickle_pure_python         | 200 us                                                 | 183 us: 1.09x faster                                                     |
| xml_etree_process          | 39.7 ms                                                | 36.5 ms: 1.09x faster                                                    |
| tomli_loads                | 1.39 sec                                               | 1.29 sec: 1.08x faster                                                   |
| sqlglot_transpile          | 1.02 ms                                                | 948 us: 1.08x faster                                                     |
| unpickle_pure_python       | 151 us                                                 | 140 us: 1.08x faster                                                     |
| asyncio_tcp                | 449 ms                                                 | 419 ms: 1.07x faster                                                     |
| regex_dna                  | 154 ms                                                 | 145 ms: 1.06x faster                                                     |
| chameleon                  | 4.70 ms                                                | 4.46 ms: 1.05x faster                                                    |
| json                       | 3.09 ms                                                | 2.94 ms: 1.05x faster                                                    |
| sqlglot_normalize          | 186 ms                                                 | 178 ms: 1.05x faster                                                     |
| spectral_norm              | 76.4 ms                                                | 73.5 ms: 1.04x faster                                                    |
| pycparser                  | 677 ms                                                 | 655 ms: 1.03x faster                                                     |
| dulwich_log                | 29.8 ms                                                | 29.0 ms: 1.03x faster                                                    |
| regex_effbot               | 2.64 ms                                                | 2.56 ms: 1.03x faster                                                    |
| xml_etree_generate         | 55.8 ms                                                | 54.3 ms: 1.03x faster                                                    |
| sympy_str                  | 148 ms                                                 | 144 ms: 1.03x faster                                                     |
| xml_etree_iterparse        | 74.0 ms                                                | 72.2 ms: 1.03x faster                                                    |
| bench_thread_pool          | 504 us                                                 | 495 us: 1.02x faster                                                     |
| scimark_monte_carlo        | 45.0 ms                                                | 44.3 ms: 1.02x faster                                                    |
| async_generators           | 304 ms                                                 | 300 ms: 1.01x faster                                                     |
| json_loads                 | 17.2 us                                                | 17.1 us: 1.01x faster                                                    |
| nqueens                    | 62.4 ms                                                | 62.0 ms: 1.01x faster                                                    |
| asyncio_websockets         | 409 ms                                                 | 408 ms: 1.00x faster                                                     |
| pidigits                   | 282 ms                                                 | 282 ms: 1.00x slower                                                     |
| mdp                        | 1.58 sec                                               | 1.58 sec: 1.00x slower                                                   |
| pickle_dict                | 18.1 us                                                | 18.1 us: 1.00x slower                                                    |
| sqlglot_optimize           | 34.0 ms                                                | 34.2 ms: 1.00x slower                                                    |
| sqlite_synth               | 1.57 us                                                | 1.58 us: 1.01x slower                                                    |
| pyflate                    | 316 ms                                                 | 319 ms: 1.01x slower                                                     |
| unpickle                   | 9.12 us                                                | 9.27 us: 1.02x slower                                                    |
| pprint_safe_repr           | 497 ms                                                 | 507 ms: 1.02x slower                                                     |
| nbody                      | 68.8 ms                                                | 70.3 ms: 1.02x slower                                                    |
| gc_traversal               | 2.40 ms                                                | 2.45 ms: 1.02x slower                                                    |
| json_dumps                 | 6.22 ms                                                | 6.37 ms: 1.02x slower                                                    |
| 2to3                       | 169 ms                                                 | 173 ms: 1.02x slower                                                     |
| pprint_pformat             | 1.01 sec                                               | 1.04 sec: 1.03x slower                                                   |
| scimark_fft                | 195 ms                                                 | 201 ms: 1.03x slower                                                     |
| go                         | 102 ms                                                 | 105 ms: 1.03x slower                                                     |
| sympy_integrate            | 11.4 ms                                                | 11.8 ms: 1.03x slower                                                    |
| bench_mp_pool              | 44.9 ms                                                | 46.4 ms: 1.04x slower                                                    |
| meteor_contest             | 71.7 ms                                                | 74.3 ms: 1.04x slower                                                    |
| pickle                     | 7.23 us                                                | 7.49 us: 1.04x slower                                                    |
| pickle_list                | 2.89 us                                                | 3.00 us: 1.04x slower                                                    |
| gunicorn                   | 1.15 ms                                                | 1.19 ms: 1.04x slower                                                    |
| pathlib                    | 24.2 ms                                                | 25.3 ms: 1.04x slower                                                    |
| docutils                   | 1.50 sec                                               | 1.58 sec: 1.05x slower                                                   |
| fannkuch                   | 248 ms                                                 | 261 ms: 1.05x slower                                                     |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.31 sec: 1.05x slower                                                   |
| aiohttp                    | 1.08 ms                                                | 1.14 ms: 1.06x slower                                                    |
| scimark_lu                 | 76.0 ms                                                | 81.3 ms: 1.07x slower                                                    |
| regex_v8                   | 16.0 ms                                                | 17.2 ms: 1.08x slower                                                    |
| regex_compile              | 77.9 ms                                                | 86.1 ms: 1.11x slower                                                    |
| mypy2                      | 380 ms                                                 | 427 ms: 1.12x slower                                                     |
| hexiom                     | 4.54 ms                                                | 5.15 ms: 1.13x slower                                                    |
| tornado_http               | 69.3 ms                                                | 79.8 ms: 1.15x slower                                                    |
| python_startup             | 11.4 ms                                                | 13.5 ms: 1.18x slower                                                    |
| coverage                   | 38.9 ms                                                | 46.5 ms: 1.20x slower                                                    |
| scimark_sor                | 87.4 ms                                                | 106 ms: 1.21x slower                                                     |
| telco                      | 3.68 ms                                                | 4.57 ms: 1.24x slower                                                    |
| python_startup_no_site     | 9.37 ms                                                | 11.7 ms: 1.25x slower                                                    |
| create_gc_cycles           | 701 us                                                 | 893 us: 1.27x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                             |

Benchmark hidden because not significant (6): sympy_expand, scimark_sparse_mat_mult, xml_etree_parse, sympy_sum, dask, unpickle_list
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (13) of results/bm-20240404-3.13.0a5+-7422720-JIT/bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 93.16% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x