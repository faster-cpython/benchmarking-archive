# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_align
- machine: darwin-arm64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.02x faster
- HPT reliability: 99.84%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 173 ms: 1.02x slower                                                 |
| chameleon      | 4.70 ms                                                | 4.52 ms: 1.04x faster                                                |
| docutils       | 1.50 sec                                               | 1.55 sec: 1.03x slower                                               |
| tornado_http   | 69.3 ms                                                | 76.8 ms: 1.11x slower                                                |
| Geometric mean | (ref)                                                  | 1.03x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization_tg  | 323 ms                                                 | 251 ms: 1.29x faster                                                 |
| async_tree_none_tg         | 258 ms                                                 | 200 ms: 1.29x faster                                                 |
| async_tree_io_tg           | 669 ms                                                 | 555 ms: 1.20x faster                                                 |
| async_tree_memoization     | 312 ms                                                 | 265 ms: 1.18x faster                                                 |
| async_tree_io              | 668 ms                                                 | 567 ms: 1.18x faster                                                 |
| async_tree_none            | 266 ms                                                 | 227 ms: 1.17x faster                                                 |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 459 ms: 1.16x faster                                                 |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 462 ms: 1.14x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.20x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 49.3 ms: 1.13x faster                                                |
| pidigits       | 282 ms                                                 | 282 ms: 1.00x slower                                                 |
| nbody          | 68.8 ms                                                | 70.1 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                  | 1.03x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 154 ms                                                 | 152 ms: 1.01x faster                                                 |
| regex_effbot   | 2.64 ms                                                | 2.62 ms: 1.01x faster                                                |
| regex_compile  | 77.9 ms                                                | 79.6 ms: 1.02x slower                                                |
| regex_v8       | 16.0 ms                                                | 17.1 ms: 1.07x slower                                                |
| Geometric mean | (ref)                                                  | 1.02x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 200 us                                                 | 183 us: 1.09x faster                                                 |
| xml_etree_process    | 39.7 ms                                                | 36.8 ms: 1.08x faster                                                |
| tomli_loads          | 1.39 sec                                               | 1.30 sec: 1.07x faster                                               |
| unpickle_pure_python | 151 us                                                 | 143 us: 1.05x faster                                                 |
| xml_etree_generate   | 55.8 ms                                                | 54.1 ms: 1.03x faster                                                |
| xml_etree_iterparse  | 74.0 ms                                                | 72.4 ms: 1.02x faster                                                |
| json_loads           | 17.2 us                                                | 17.0 us: 1.02x faster                                                |
| xml_etree_parse      | 106 ms                                                 | 105 ms: 1.01x faster                                                 |
| pickle_dict          | 18.1 us                                                | 18.1 us: 1.00x slower                                                |
| unpickle_list        | 3.02 us                                                | 3.06 us: 1.01x slower                                                |
| json_dumps           | 6.22 ms                                                | 6.32 ms: 1.02x slower                                                |
| pickle               | 7.23 us                                                | 7.41 us: 1.03x slower                                                |
| pickle_list          | 2.89 us                                                | 2.98 us: 1.03x slower                                                |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 11.4 ms                                                | 13.3 ms: 1.17x slower                                                |
| python_startup_no_site | 9.37 ms                                                | 11.6 ms: 1.23x slower                                                |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 7.71 ms                                                | 6.92 ms: 1.11x faster                                                |
| django_template | 22.3 ms                                                | 20.7 ms: 1.08x faster                                                |
| Geometric mean  | (ref)                                                  | 1.10x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 93.0 us                                                | 69.7 us: 1.33x faster                                                |
| async_tree_memoization_tg  | 323 ms                                                 | 251 ms: 1.29x faster                                                 |
| async_tree_none_tg         | 258 ms                                                 | 200 ms: 1.29x faster                                                 |
| async_tree_io_tg           | 669 ms                                                 | 555 ms: 1.20x faster                                                 |
| comprehensions             | 14.5 us                                                | 12.1 us: 1.20x faster                                                |
| raytrace                   | 212 ms                                                 | 178 ms: 1.19x faster                                                 |
| async_tree_memoization     | 312 ms                                                 | 265 ms: 1.18x faster                                                 |
| async_tree_io              | 668 ms                                                 | 567 ms: 1.18x faster                                                 |
| generators                 | 31.1 ms                                                | 26.4 ms: 1.18x faster                                                |
| async_tree_none            | 266 ms                                                 | 227 ms: 1.17x faster                                                 |
| logging_silent             | 76.4 ns                                                | 65.7 ns: 1.16x faster                                                |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 459 ms: 1.16x faster                                                 |
| deltablue                  | 2.71 ms                                                | 2.35 ms: 1.15x faster                                                |
| coroutines                 | 19.2 ms                                                | 16.9 ms: 1.14x faster                                                |
| deepcopy_memo              | 27.7 us                                                | 24.2 us: 1.14x faster                                                |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 462 ms: 1.14x faster                                                 |
| float                      | 55.8 ms                                                | 49.3 ms: 1.13x faster                                                |
| logging_simple             | 3.69 us                                                | 3.27 us: 1.13x faster                                                |
| mako                       | 7.71 ms                                                | 6.92 ms: 1.11x faster                                                |
| deepcopy_reduce            | 2.07 us                                                | 1.86 us: 1.11x faster                                                |
| logging_format             | 3.98 us                                                | 3.59 us: 1.11x faster                                                |
| chaos                      | 42.5 ms                                                | 38.3 ms: 1.11x faster                                                |
| sqlglot_parse              | 848 us                                                 | 765 us: 1.11x faster                                                 |
| deepcopy                   | 235 us                                                 | 212 us: 1.11x faster                                                 |
| crypto_pyaes               | 51.9 ms                                                | 46.9 ms: 1.11x faster                                                |
| sqlglot_transpile          | 1.02 ms                                                | 935 us: 1.09x faster                                                 |
| pickle_pure_python         | 200 us                                                 | 183 us: 1.09x faster                                                 |
| django_template            | 22.3 ms                                                | 20.7 ms: 1.08x faster                                                |
| xml_etree_process          | 39.7 ms                                                | 36.8 ms: 1.08x faster                                                |
| tomli_loads                | 1.39 sec                                               | 1.30 sec: 1.07x faster                                               |
| sqlglot_normalize          | 186 ms                                                 | 176 ms: 1.06x faster                                                 |
| sympy_str                  | 148 ms                                                 | 140 ms: 1.06x faster                                                 |
| unpickle_pure_python       | 151 us                                                 | 143 us: 1.05x faster                                                 |
| richards_super             | 36.0 ms                                                | 34.5 ms: 1.05x faster                                                |
| json                       | 3.09 ms                                                | 2.97 ms: 1.04x faster                                                |
| chameleon                  | 4.70 ms                                                | 4.52 ms: 1.04x faster                                                |
| spectral_norm              | 76.4 ms                                                | 73.8 ms: 1.03x faster                                                |
| xml_etree_generate         | 55.8 ms                                                | 54.1 ms: 1.03x faster                                                |
| richards                   | 32.1 ms                                                | 31.2 ms: 1.03x faster                                                |
| scimark_monte_carlo        | 45.0 ms                                                | 43.8 ms: 1.03x faster                                                |
| pprint_safe_repr           | 497 ms                                                 | 483 ms: 1.03x faster                                                 |
| sympy_sum                  | 77.6 ms                                                | 75.5 ms: 1.03x faster                                                |
| pprint_pformat             | 1.01 sec                                               | 986 ms: 1.03x faster                                                 |
| nqueens                    | 62.4 ms                                                | 60.9 ms: 1.03x faster                                                |
| bench_thread_pool          | 504 us                                                 | 492 us: 1.02x faster                                                 |
| pycparser                  | 677 ms                                                 | 661 ms: 1.02x faster                                                 |
| sympy_expand               | 241 ms                                                 | 236 ms: 1.02x faster                                                 |
| xml_etree_iterparse        | 74.0 ms                                                | 72.4 ms: 1.02x faster                                                |
| json_loads                 | 17.2 us                                                | 17.0 us: 1.02x faster                                                |
| regex_dna                  | 154 ms                                                 | 152 ms: 1.01x faster                                                 |
| sqlglot_optimize           | 34.0 ms                                                | 33.6 ms: 1.01x faster                                                |
| xml_etree_parse            | 106 ms                                                 | 105 ms: 1.01x faster                                                 |
| async_generators           | 304 ms                                                 | 302 ms: 1.01x faster                                                 |
| sympy_integrate            | 11.4 ms                                                | 11.3 ms: 1.01x faster                                                |
| regex_effbot               | 2.64 ms                                                | 2.62 ms: 1.01x faster                                                |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 3.12 ms: 1.01x faster                                                |
| mdp                        | 1.58 sec                                               | 1.58 sec: 1.00x faster                                               |
| asyncio_websockets         | 409 ms                                                 | 409 ms: 1.00x faster                                                 |
| pickle_dict                | 18.1 us                                                | 18.1 us: 1.00x slower                                                |
| pidigits                   | 282 ms                                                 | 282 ms: 1.00x slower                                                 |
| sqlite_synth               | 1.57 us                                                | 1.58 us: 1.00x slower                                                |
| dulwich_log                | 29.8 ms                                                | 30.0 ms: 1.01x slower                                                |
| unpickle_list              | 3.02 us                                                | 3.06 us: 1.01x slower                                                |
| json_dumps                 | 6.22 ms                                                | 6.32 ms: 1.02x slower                                                |
| gc_traversal               | 2.40 ms                                                | 2.45 ms: 1.02x slower                                                |
| nbody                      | 68.8 ms                                                | 70.1 ms: 1.02x slower                                                |
| 2to3                       | 169 ms                                                 | 173 ms: 1.02x slower                                                 |
| regex_compile              | 77.9 ms                                                | 79.6 ms: 1.02x slower                                                |
| pickle                     | 7.23 us                                                | 7.41 us: 1.03x slower                                                |
| go                         | 102 ms                                                 | 104 ms: 1.03x slower                                                 |
| meteor_contest             | 71.7 ms                                                | 73.9 ms: 1.03x slower                                                |
| pickle_list                | 2.89 us                                                | 2.98 us: 1.03x slower                                                |
| scimark_fft                | 195 ms                                                 | 202 ms: 1.03x slower                                                 |
| bench_mp_pool              | 44.9 ms                                                | 46.4 ms: 1.03x slower                                                |
| docutils                   | 1.50 sec                                               | 1.55 sec: 1.03x slower                                               |
| aiohttp                    | 1.08 ms                                                | 1.12 ms: 1.04x slower                                                |
| pyflate                    | 316 ms                                                 | 328 ms: 1.04x slower                                                 |
| fannkuch                   | 248 ms                                                 | 259 ms: 1.04x slower                                                 |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.30 sec: 1.05x slower                                               |
| regex_v8                   | 16.0 ms                                                | 17.1 ms: 1.07x slower                                                |
| mypy2                      | 380 ms                                                 | 410 ms: 1.08x slower                                                 |
| hexiom                     | 4.54 ms                                                | 4.91 ms: 1.08x slower                                                |
| scimark_lu                 | 76.0 ms                                                | 82.4 ms: 1.08x slower                                                |
| tornado_http               | 69.3 ms                                                | 76.8 ms: 1.11x slower                                                |
| python_startup             | 11.4 ms                                                | 13.3 ms: 1.17x slower                                                |
| create_gc_cycles           | 701 us                                                 | 844 us: 1.20x slower                                                 |
| coverage                   | 38.9 ms                                                | 47.0 ms: 1.21x slower                                                |
| scimark_sor                | 87.4 ms                                                | 108 ms: 1.23x slower                                                 |
| python_startup_no_site     | 9.37 ms                                                | 11.6 ms: 1.23x slower                                                |
| telco                      | 3.68 ms                                                | 4.54 ms: 1.23x slower                                                |
| unpack_sequence            | 31.5 ns                                                | 115 ns: 3.66x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (5): asyncio_tcp, pathlib, dask, unpickle, gunicorn
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (13) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.84% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x