# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 752e183
- commit date: 2024-03-31
- overall geometric mean: 1.01x slower
- HPT reliability: 99.53%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 267 ms                                                                 | 269 ms: 1.01x slower                                   |
| html5lib       | 68.0 ms                                                                | 67.0 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                           |

Benchmark hidden because not significant (3): chameleon, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 190 ms                                                                 | 190 ms: 1.00x faster                                   |
| float          | 76.6 ms                                                                | 77.2 ms: 1.01x slower                                  |
| nbody          | 87.9 ms                                                                | 89.5 ms: 1.02x slower                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_dna      | 225 ms                                                                 | 222 ms: 1.01x faster                                   |
| regex_compile  | 134 ms                                                                 | 134 ms: 1.00x faster                                   |
| regex_v8       | 25.3 ms                                                                | 26.2 ms: 1.03x slower                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| unpickle_list        | 5.19 us                                                                | 5.13 us: 1.01x faster                                  |
| pickle               | 11.7 us                                                                | 11.6 us: 1.01x faster                                  |
| pickle_list          | 5.00 us                                                                | 4.96 us: 1.01x faster                                  |
| xml_etree_generate   | 85.9 ms                                                                | 86.7 ms: 1.01x slower                                  |
| unpickle_pure_python | 217 us                                                                 | 220 us: 1.01x slower                                   |
| tomli_loads          | 2.19 sec                                                               | 2.22 sec: 1.01x slower                                 |
| pickle_pure_python   | 297 us                                                                 | 303 us: 1.02x slower                                   |
| pickle_dict          | 33.0 us                                                                | 33.6 us: 1.02x slower                                  |
| unpickle             | 15.9 us                                                                | 18.5 us: 1.16x slower                                  |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                           |

Benchmark hidden because not significant (5): xml_etree_parse, json_dumps, json_loads, xml_etree_iterparse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 9.03 ms                                                                | 8.99 ms: 1.00x faster                                  |
| python_startup         | 10.7 ms                                                                | 10.6 ms: 1.00x faster                                  |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                                | 52.6 ms: 1.01x faster                                  |
| genshi_text    | 24.6 ms                                                                | 24.3 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                | bm-20240329-linux-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|--------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| crypto_pyaes             | 74.0 ms                                                                | 72.1 ms: 1.03x faster                                  |
| html5lib                 | 68.0 ms                                                                | 67.0 ms: 1.02x faster                                  |
| genshi_xml               | 53.4 ms                                                                | 52.6 ms: 1.01x faster                                  |
| scimark_sparse_mat_mult  | 4.78 ms                                                                | 4.71 ms: 1.01x faster                                  |
| typing_runtime_protocols | 114 us                                                                 | 112 us: 1.01x faster                                   |
| json                     | 5.39 ms                                                                | 5.33 ms: 1.01x faster                                  |
| regex_dna                | 225 ms                                                                 | 222 ms: 1.01x faster                                   |
| unpickle_list            | 5.19 us                                                                | 5.13 us: 1.01x faster                                  |
| genshi_text              | 24.6 ms                                                                | 24.3 ms: 1.01x faster                                  |
| nqueens                  | 80.4 ms                                                                | 79.6 ms: 1.01x faster                                  |
| pickle                   | 11.7 us                                                                | 11.6 us: 1.01x faster                                  |
| pickle_list              | 5.00 us                                                                | 4.96 us: 1.01x faster                                  |
| python_startup_no_site   | 9.03 ms                                                                | 8.99 ms: 1.00x faster                                  |
| regex_compile            | 134 ms                                                                 | 134 ms: 1.00x faster                                   |
| pyflate                  | 462 ms                                                                 | 460 ms: 1.00x faster                                   |
| python_startup           | 10.7 ms                                                                | 10.6 ms: 1.00x faster                                  |
| asyncio_tcp_ssl          | 1.84 sec                                                               | 1.83 sec: 1.00x faster                                 |
| pidigits                 | 190 ms                                                                 | 190 ms: 1.00x faster                                   |
| pylint                   | 279 ms                                                                 | 280 ms: 1.00x slower                                   |
| deltablue                | 3.20 ms                                                                | 3.21 ms: 1.00x slower                                  |
| mdp                      | 2.58 sec                                                               | 2.60 sec: 1.01x slower                                 |
| logging_simple           | 5.87 us                                                                | 5.90 us: 1.01x slower                                  |
| aiohttp                  | 1.17 ms                                                                | 1.18 ms: 1.01x slower                                  |
| sqlglot_parse            | 1.27 ms                                                                | 1.28 ms: 1.01x slower                                  |
| sqlglot_transpile        | 1.58 ms                                                                | 1.59 ms: 1.01x slower                                  |
| sympy_expand             | 461 ms                                                                 | 464 ms: 1.01x slower                                   |
| generators               | 29.6 ms                                                                | 29.8 ms: 1.01x slower                                  |
| thrift                   | 810 us                                                                 | 816 us: 1.01x slower                                   |
| deepcopy                 | 350 us                                                                 | 353 us: 1.01x slower                                   |
| sqlite_synth             | 2.88 us                                                                | 2.90 us: 1.01x slower                                  |
| float                    | 76.6 ms                                                                | 77.2 ms: 1.01x slower                                  |
| richards_super           | 52.2 ms                                                                | 52.6 ms: 1.01x slower                                  |
| 2to3                     | 267 ms                                                                 | 269 ms: 1.01x slower                                   |
| bench_thread_pool        | 823 us                                                                 | 830 us: 1.01x slower                                   |
| sympy_integrate          | 19.9 ms                                                                | 20.0 ms: 1.01x slower                                  |
| sqlglot_optimize         | 54.3 ms                                                                | 54.8 ms: 1.01x slower                                  |
| sqlglot_normalize        | 108 ms                                                                 | 110 ms: 1.01x slower                                   |
| logging_silent           | 99.5 ns                                                                | 100 ns: 1.01x slower                                   |
| richards                 | 45.4 ms                                                                | 45.9 ms: 1.01x slower                                  |
| xml_etree_generate       | 85.9 ms                                                                | 86.7 ms: 1.01x slower                                  |
| logging_format           | 6.49 us                                                                | 6.56 us: 1.01x slower                                  |
| asyncio_tcp              | 500 ms                                                                 | 506 ms: 1.01x slower                                   |
| go                       | 138 ms                                                                 | 140 ms: 1.01x slower                                   |
| unpickle_pure_python     | 217 us                                                                 | 220 us: 1.01x slower                                   |
| tomli_loads              | 2.19 sec                                                               | 2.22 sec: 1.01x slower                                 |
| hexiom                   | 6.09 ms                                                                | 6.18 ms: 1.02x slower                                  |
| deepcopy_reduce          | 3.10 us                                                                | 3.15 us: 1.02x slower                                  |
| chaos                    | 59.5 ms                                                                | 60.4 ms: 1.02x slower                                  |
| pickle_pure_python       | 297 us                                                                 | 303 us: 1.02x slower                                   |
| nbody                    | 87.9 ms                                                                | 89.5 ms: 1.02x slower                                  |
| raytrace                 | 263 ms                                                                 | 268 ms: 1.02x slower                                   |
| pickle_dict              | 33.0 us                                                                | 33.6 us: 1.02x slower                                  |
| fannkuch                 | 380 ms                                                                 | 387 ms: 1.02x slower                                   |
| gc_traversal             | 3.91 ms                                                                | 4.00 ms: 1.02x slower                                  |
| scimark_sor              | 121 ms                                                                 | 124 ms: 1.03x slower                                   |
| deepcopy_memo            | 37.0 us                                                                | 38.3 us: 1.03x slower                                  |
| regex_v8                 | 25.3 ms                                                                | 26.2 ms: 1.03x slower                                  |
| scimark_lu               | 113 ms                                                                 | 117 ms: 1.03x slower                                   |
| coroutines               | 22.5 ms                                                                | 23.5 ms: 1.04x slower                                  |
| pycparser                | 1.17 sec                                                               | 1.22 sec: 1.04x slower                                 |
| scimark_fft              | 363 ms                                                                 | 381 ms: 1.05x slower                                   |
| unpickle                 | 15.9 us                                                                | 18.5 us: 1.16x slower                                  |
| unpack_sequence          | 44.8 ns                                                                | 53.9 ns: 1.20x slower                                  |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                           |

Benchmark hidden because not significant (39): async_tree_cpu_io_mixed, async_tree_none, async_tree_cpu_io_mixed_tg, spectral_norm, async_tree_io, regex_effbot, docutils, pprint_safe_repr, pprint_pformat, django_template, xml_etree_parse, chameleon, mako, asyncio_websockets, async_generators, scimark_monte_carlo, json_dumps, meteor_contest, comprehensions, json_loads, gunicorn, dulwich_log, create_gc_cycles, tornado_http, async_tree_none_tg, sympy_str, dask, xml_etree_iterparse, async_tree_memoization_tg, mypy2, sympy_sum, bench_mp_pool, xml_etree_process, coverage, async_tree_memoization, async_tree_io_tg, pathlib, telco, djangocms

# HPT report

- Reliability score: 99.53% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x