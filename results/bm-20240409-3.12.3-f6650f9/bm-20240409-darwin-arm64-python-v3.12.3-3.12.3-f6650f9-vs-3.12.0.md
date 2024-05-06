# Results vs. 3.12.0

- fork: python
- ref: v3.12.3
- machine: darwin-arm64
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.00x faster
- HPT reliability: 87.63%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 169 ms                                                 | 168 ms: 1.01x faster                                   |
| chameleon      | 4.70 ms                                                | 4.65 ms: 1.01x faster                                  |
| docutils       | 1.50 sec                                               | 1.49 sec: 1.01x faster                                 |
| tornado_http   | 69.3 ms                                                | 75.9 ms: 1.10x slower                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io          | 668 ms                                                 | 671 ms: 1.01x slower                                   |
| async_tree_memoization | 312 ms                                                 | 315 ms: 1.01x slower                                   |
| async_tree_io_tg       | 669 ms                                                 | 677 ms: 1.01x slower                                   |
| async_tree_none_tg     | 258 ms                                                 | 261 ms: 1.01x slower                                   |
| async_tree_none        | 266 ms                                                 | 269 ms: 1.01x slower                                   |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 68.8 ms                                                | 67.4 ms: 1.02x faster                                  |
| float          | 55.8 ms                                                | 55.6 ms: 1.00x faster                                  |
| pidigits       | 282 ms                                                 | 283 ms: 1.00x slower                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_dna      | 154 ms                                                 | 152 ms: 1.01x faster                                   |
| regex_compile  | 77.9 ms                                                | 77.6 ms: 1.00x faster                                  |
| regex_effbot   | 2.64 ms                                                | 2.68 ms: 1.02x slower                                  |
| regex_v8       | 16.0 ms                                                | 16.7 ms: 1.05x slower                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| unpickle_pure_python | 151 us                                                 | 149 us: 1.01x faster                                   |
| xml_etree_process    | 39.7 ms                                                | 39.8 ms: 1.00x slower                                  |
| xml_etree_generate   | 55.8 ms                                                | 56.2 ms: 1.01x slower                                  |
| json_dumps           | 6.22 ms                                                | 6.26 ms: 1.01x slower                                  |
| pickle_pure_python   | 200 us                                                 | 201 us: 1.01x slower                                   |
| json_loads           | 17.2 us                                                | 17.4 us: 1.01x slower                                  |
| xml_etree_iterparse  | 74.0 ms                                                | 74.8 ms: 1.01x slower                                  |
| pickle               | 7.23 us                                                | 7.35 us: 1.02x slower                                  |
| unpickle_list        | 3.02 us                                                | 3.08 us: 1.02x slower                                  |
| unpickle             | 9.12 us                                                | 9.38 us: 1.03x slower                                  |
| Geometric mean       | (ref)                                                  | 1.01x slower                                           |

Benchmark hidden because not significant (4): tomli_loads, pickle_dict, pickle_list, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 9.37 ms                                                | 8.97 ms: 1.05x faster                                  |
| python_startup         | 11.4 ms                                                | 11.2 ms: 1.01x faster                                  |
| Geometric mean         | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 7.71 ms                                                | 7.60 ms: 1.01x faster                                  |
| django_template | 22.3 ms                                                | 22.4 ms: 1.00x slower                                  |
| Geometric mean  | (ref)                                                  | 1.01x faster                                           |

All benchmarks:
===============

| Benchmark                | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols | 93.0 us                                                | 73.5 us: 1.27x faster                                  |
| comprehensions           | 14.5 us                                                | 11.7 us: 1.25x faster                                  |
| asyncio_tcp              | 449 ms                                                 | 408 ms: 1.10x faster                                   |
| gunicorn                 | 1.15 ms                                                | 1.06 ms: 1.08x faster                                  |
| aiohttp                  | 1.08 ms                                                | 1.01 ms: 1.07x faster                                  |
| sympy_sum                | 77.6 ms                                                | 74.2 ms: 1.05x faster                                  |
| sympy_str                | 148 ms                                                 | 141 ms: 1.05x faster                                   |
| python_startup_no_site   | 9.37 ms                                                | 8.97 ms: 1.05x faster                                  |
| sympy_integrate          | 11.4 ms                                                | 10.9 ms: 1.04x faster                                  |
| coroutines               | 19.2 ms                                                | 18.8 ms: 1.02x faster                                  |
| nbody                    | 68.8 ms                                                | 67.4 ms: 1.02x faster                                  |
| bench_mp_pool            | 44.9 ms                                                | 44.0 ms: 1.02x faster                                  |
| deepcopy                 | 235 us                                                 | 230 us: 1.02x faster                                   |
| generators               | 31.1 ms                                                | 30.5 ms: 1.02x faster                                  |
| deepcopy_reduce          | 2.07 us                                                | 2.03 us: 1.02x faster                                  |
| dulwich_log              | 29.8 ms                                                | 29.3 ms: 1.02x faster                                  |
| mako                     | 7.71 ms                                                | 7.60 ms: 1.01x faster                                  |
| regex_dna                | 154 ms                                                 | 152 ms: 1.01x faster                                   |
| python_startup           | 11.4 ms                                                | 11.2 ms: 1.01x faster                                  |
| scimark_lu               | 76.0 ms                                                | 75.0 ms: 1.01x faster                                  |
| bench_thread_pool        | 504 us                                                 | 498 us: 1.01x faster                                   |
| deltablue                | 2.71 ms                                                | 2.67 ms: 1.01x faster                                  |
| json                     | 3.09 ms                                                | 3.06 ms: 1.01x faster                                  |
| unpickle_pure_python     | 151 us                                                 | 149 us: 1.01x faster                                   |
| docutils                 | 1.50 sec                                               | 1.49 sec: 1.01x faster                                 |
| create_gc_cycles         | 701 us                                                 | 695 us: 1.01x faster                                   |
| chameleon                | 4.70 ms                                                | 4.65 ms: 1.01x faster                                  |
| async_generators         | 304 ms                                                 | 301 ms: 1.01x faster                                   |
| 2to3                     | 169 ms                                                 | 168 ms: 1.01x faster                                   |
| raytrace                 | 212 ms                                                 | 211 ms: 1.01x faster                                   |
| deepcopy_memo            | 27.7 us                                                | 27.5 us: 1.01x faster                                  |
| float                    | 55.8 ms                                                | 55.6 ms: 1.00x faster                                  |
| regex_compile            | 77.9 ms                                                | 77.6 ms: 1.00x faster                                  |
| richards                 | 32.1 ms                                                | 32.0 ms: 1.00x faster                                  |
| spectral_norm            | 76.4 ms                                                | 76.2 ms: 1.00x faster                                  |
| asyncio_websockets       | 409 ms                                                 | 408 ms: 1.00x faster                                   |
| gc_traversal             | 2.40 ms                                                | 2.40 ms: 1.00x faster                                  |
| sympy_expand             | 241 ms                                                 | 241 ms: 1.00x faster                                   |
| mdp                      | 1.58 sec                                               | 1.58 sec: 1.00x slower                                 |
| hexiom                   | 4.54 ms                                                | 4.55 ms: 1.00x slower                                  |
| pprint_pformat           | 1.01 sec                                               | 1.01 sec: 1.00x slower                                 |
| django_template          | 22.3 ms                                                | 22.4 ms: 1.00x slower                                  |
| sqlglot_optimize         | 34.0 ms                                                | 34.1 ms: 1.00x slower                                  |
| richards_super           | 36.0 ms                                                | 36.1 ms: 1.00x slower                                  |
| sqlglot_normalize        | 186 ms                                                 | 186 ms: 1.00x slower                                   |
| sqlalchemy_declarative   | 62.3 ms                                                | 62.5 ms: 1.00x slower                                  |
| xml_etree_process        | 39.7 ms                                                | 39.8 ms: 1.00x slower                                  |
| sqlglot_transpile        | 1.02 ms                                                | 1.02 ms: 1.00x slower                                  |
| sqlglot_parse            | 848 us                                                 | 851 us: 1.00x slower                                   |
| pidigits                 | 282 ms                                                 | 283 ms: 1.00x slower                                   |
| logging_format           | 3.98 us                                                | 4.00 us: 1.00x slower                                  |
| fannkuch                 | 248 ms                                                 | 250 ms: 1.00x slower                                   |
| sqlalchemy_imperative    | 6.68 ms                                                | 6.71 ms: 1.00x slower                                  |
| async_tree_io            | 668 ms                                                 | 671 ms: 1.01x slower                                   |
| scimark_sparse_mat_mult  | 3.14 ms                                                | 3.15 ms: 1.01x slower                                  |
| chaos                    | 42.5 ms                                                | 42.8 ms: 1.01x slower                                  |
| sqlite_synth             | 1.57 us                                                | 1.58 us: 1.01x slower                                  |
| xml_etree_generate       | 55.8 ms                                                | 56.2 ms: 1.01x slower                                  |
| json_dumps               | 6.22 ms                                                | 6.26 ms: 1.01x slower                                  |
| coverage                 | 38.9 ms                                                | 39.1 ms: 1.01x slower                                  |
| pickle_pure_python       | 200 us                                                 | 201 us: 1.01x slower                                   |
| json_loads               | 17.2 us                                                | 17.4 us: 1.01x slower                                  |
| logging_simple           | 3.69 us                                                | 3.71 us: 1.01x slower                                  |
| pyflate                  | 316 ms                                                 | 318 ms: 1.01x slower                                   |
| async_tree_memoization   | 312 ms                                                 | 315 ms: 1.01x slower                                   |
| pprint_safe_repr         | 497 ms                                                 | 502 ms: 1.01x slower                                   |
| scimark_sor              | 87.4 ms                                                | 88.2 ms: 1.01x slower                                  |
| xml_etree_iterparse      | 74.0 ms                                                | 74.8 ms: 1.01x slower                                  |
| async_tree_io_tg         | 669 ms                                                 | 677 ms: 1.01x slower                                   |
| async_tree_none_tg       | 258 ms                                                 | 261 ms: 1.01x slower                                   |
| nqueens                  | 62.4 ms                                                | 63.2 ms: 1.01x slower                                  |
| scimark_monte_carlo      | 45.0 ms                                                | 45.6 ms: 1.01x slower                                  |
| scimark_fft              | 195 ms                                                 | 198 ms: 1.01x slower                                   |
| async_tree_none          | 266 ms                                                 | 269 ms: 1.01x slower                                   |
| regex_effbot             | 2.64 ms                                                | 2.68 ms: 1.02x slower                                  |
| pickle                   | 7.23 us                                                | 7.35 us: 1.02x slower                                  |
| meteor_contest           | 71.7 ms                                                | 73.1 ms: 1.02x slower                                  |
| unpickle_list            | 3.02 us                                                | 3.08 us: 1.02x slower                                  |
| telco                    | 3.68 ms                                                | 3.76 ms: 1.02x slower                                  |
| unpickle                 | 9.12 us                                                | 9.38 us: 1.03x slower                                  |
| logging_silent           | 76.4 ns                                                | 78.7 ns: 1.03x slower                                  |
| pathlib                  | 24.2 ms                                                | 25.3 ms: 1.04x slower                                  |
| regex_v8                 | 16.0 ms                                                | 16.7 ms: 1.05x slower                                  |
| tornado_http             | 69.3 ms                                                | 75.9 ms: 1.10x slower                                  |
| asyncio_tcp_ssl          | 1.24 sec                                               | 1.41 sec: 1.13x slower                                 |
| mypy2                    | 380 ms                                                 | 457 ms: 1.20x slower                                   |
| Geometric mean           | (ref)                                                  | 1.00x faster                                           |

Benchmark hidden because not significant (11): tomli_loads, dask, async_tree_cpu_io_mixed, crypto_pyaes, go, pickle_dict, pickle_list, async_tree_cpu_io_mixed_tg, pycparser, xml_etree_parse, async_tree_memoization_tg
Ignored benchmarks (1) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: unpack_sequence
Ignored benchmarks (13) of results/bm-20240409-3.12.3-f6650f9/bm-20240409-darwin-arm64-python-v3.12.3-3.12.3-f6650f9.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 87.63% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.97x