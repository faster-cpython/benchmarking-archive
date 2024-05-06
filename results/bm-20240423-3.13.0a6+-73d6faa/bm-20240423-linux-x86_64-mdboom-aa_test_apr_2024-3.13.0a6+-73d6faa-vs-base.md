# Results vs. base

- fork: mdboom
- ref: aa_test_apr_2024
- machine: linux-x86_64
- commit hash: 73d6faa
- commit date: 2024-04-23
- overall geometric mean: 1.00x slower
- HPT reliability: 99.79%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6+-2584082 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 269 ms                                                                 | 271 ms: 1.01x slower                                               |
| chameleon      | 7.04 ms                                                                | 6.90 ms: 1.02x faster                                              |
| docutils       | 2.80 sec                                                               | 2.81 sec: 1.00x slower                                             |
| html5lib       | 65.7 ms                                                                | 67.4 ms: 1.03x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                       |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6+-2584082 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io  | 933 ms                                                                 | 908 ms: 1.03x faster                                               |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                       |

Benchmark hidden because not significant (7): async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6+-2584082 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits       | 206 ms                                                                 | 190 ms: 1.09x faster                                               |
| float          | 78.1 ms                                                                | 79.2 ms: 1.01x slower                                              |
| nbody          | 89.4 ms                                                                | 95.5 ms: 1.07x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6+-2584082 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.88 ms                                                                | 3.73 ms: 1.04x faster                                              |
| regex_dna      | 233 ms                                                                 | 225 ms: 1.04x faster                                               |
| regex_v8       | 25.4 ms                                                                | 25.8 ms: 1.01x slower                                              |
| regex_compile  | 134 ms                                                                 | 136 ms: 1.02x slower                                               |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6+-2584082 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| unpickle_list        | 5.46 us                                                                | 5.11 us: 1.07x faster                                              |
| pickle_dict          | 35.7 us                                                                | 35.3 us: 1.01x faster                                              |
| pickle_list          | 5.10 us                                                                | 5.07 us: 1.00x faster                                              |
| json_dumps           | 10.6 ms                                                                | 10.6 ms: 1.00x slower                                              |
| xml_etree_process    | 60.1 ms                                                                | 60.4 ms: 1.01x slower                                              |
| pickle_pure_python   | 304 us                                                                 | 306 us: 1.01x slower                                               |
| xml_etree_generate   | 86.7 ms                                                                | 87.7 ms: 1.01x slower                                              |
| json_loads           | 27.5 us                                                                | 27.8 us: 1.01x slower                                              |
| tomli_loads          | 2.17 sec                                                               | 2.21 sec: 1.02x slower                                             |
| unpickle_pure_python | 215 us                                                                 | 219 us: 1.02x slower                                               |
| xml_etree_iterparse  | 106 ms                                                                 | 108 ms: 1.02x slower                                               |
| unpickle             | 15.3 us                                                                | 15.6 us: 1.02x slower                                              |
| pickle               | 11.9 us                                                                | 12.1 us: 1.02x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                       |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6+-2584082 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup | 10.5 ms                                                                | 10.5 ms: 1.00x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                       |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6+-2584082 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_xml     | 51.6 ms                                                                | 51.9 ms: 1.01x slower                                              |
| genshi_text    | 23.5 ms                                                                | 23.9 ms: 1.02x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                       |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                | bm-20240423-linux-x86_64-python-258408239a4fe8a14919-3.13.0a6+-2584082 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|--------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits                 | 206 ms                                                                 | 190 ms: 1.09x faster                                               |
| unpickle_list            | 5.46 us                                                                | 5.11 us: 1.07x faster                                              |
| mdp                      | 2.76 sec                                                               | 2.60 sec: 1.06x faster                                             |
| scimark_sor              | 130 ms                                                                 | 124 ms: 1.05x faster                                               |
| regex_effbot             | 3.88 ms                                                                | 3.73 ms: 1.04x faster                                              |
| regex_dna                | 233 ms                                                                 | 225 ms: 1.04x faster                                               |
| async_tree_io            | 933 ms                                                                 | 908 ms: 1.03x faster                                               |
| generators               | 30.5 ms                                                                | 29.8 ms: 1.02x faster                                              |
| pyflate                  | 480 ms                                                                 | 469 ms: 1.02x faster                                               |
| chameleon                | 7.04 ms                                                                | 6.90 ms: 1.02x faster                                              |
| thrift                   | 824 us                                                                 | 809 us: 1.02x faster                                               |
| meteor_contest           | 112 ms                                                                 | 111 ms: 1.02x faster                                               |
| async_generators         | 451 ms                                                                 | 444 ms: 1.01x faster                                               |
| deepcopy_reduce          | 3.23 us                                                                | 3.19 us: 1.01x faster                                              |
| fannkuch                 | 400 ms                                                                 | 396 ms: 1.01x faster                                               |
| pickle_dict              | 35.7 us                                                                | 35.3 us: 1.01x faster                                              |
| typing_runtime_protocols | 115 us                                                                 | 113 us: 1.01x faster                                               |
| coroutines               | 23.0 ms                                                                | 22.8 ms: 1.01x faster                                              |
| asyncio_tcp              | 508 ms                                                                 | 505 ms: 1.01x faster                                               |
| pickle_list              | 5.10 us                                                                | 5.07 us: 1.00x faster                                              |
| create_gc_cycles         | 1.75 ms                                                                | 1.75 ms: 1.00x faster                                              |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.85 sec: 1.00x slower                                             |
| bench_thread_pool        | 831 us                                                                 | 833 us: 1.00x slower                                               |
| python_startup           | 10.5 ms                                                                | 10.5 ms: 1.00x slower                                              |
| raytrace                 | 263 ms                                                                 | 264 ms: 1.00x slower                                               |
| crypto_pyaes             | 74.7 ms                                                                | 75.1 ms: 1.00x slower                                              |
| json_dumps               | 10.6 ms                                                                | 10.6 ms: 1.00x slower                                              |
| docutils                 | 2.80 sec                                                               | 2.81 sec: 1.00x slower                                             |
| sqlglot_transpile        | 1.59 ms                                                                | 1.60 ms: 1.01x slower                                              |
| xml_etree_process        | 60.1 ms                                                                | 60.4 ms: 1.01x slower                                              |
| genshi_xml               | 51.6 ms                                                                | 51.9 ms: 1.01x slower                                              |
| sqlite_synth             | 2.93 us                                                                | 2.95 us: 1.01x slower                                              |
| deepcopy                 | 354 us                                                                 | 357 us: 1.01x slower                                               |
| logging_format           | 6.44 us                                                                | 6.49 us: 1.01x slower                                              |
| 2to3                     | 269 ms                                                                 | 271 ms: 1.01x slower                                               |
| sympy_integrate          | 20.2 ms                                                                | 20.4 ms: 1.01x slower                                              |
| pickle_pure_python       | 304 us                                                                 | 306 us: 1.01x slower                                               |
| sqlglot_parse            | 1.28 ms                                                                | 1.29 ms: 1.01x slower                                              |
| nqueens                  | 79.7 ms                                                                | 80.5 ms: 1.01x slower                                              |
| deepcopy_memo            | 38.1 us                                                                | 38.5 us: 1.01x slower                                              |
| deltablue                | 3.23 ms                                                                | 3.27 ms: 1.01x slower                                              |
| xml_etree_generate       | 86.7 ms                                                                | 87.7 ms: 1.01x slower                                              |
| dulwich_log              | 66.0 ms                                                                | 66.8 ms: 1.01x slower                                              |
| sympy_str                | 278 ms                                                                 | 281 ms: 1.01x slower                                               |
| json_loads               | 27.5 us                                                                | 27.8 us: 1.01x slower                                              |
| sympy_sum                | 155 ms                                                                 | 157 ms: 1.01x slower                                               |
| hexiom                   | 6.27 ms                                                                | 6.35 ms: 1.01x slower                                              |
| pprint_pformat           | 1.52 sec                                                               | 1.54 sec: 1.01x slower                                             |
| regex_v8                 | 25.4 ms                                                                | 25.8 ms: 1.01x slower                                              |
| go                       | 142 ms                                                                 | 144 ms: 1.01x slower                                               |
| float                    | 78.1 ms                                                                | 79.2 ms: 1.01x slower                                              |
| sympy_expand             | 468 ms                                                                 | 475 ms: 1.01x slower                                               |
| sqlglot_optimize         | 54.4 ms                                                                | 55.2 ms: 1.01x slower                                              |
| regex_compile            | 134 ms                                                                 | 136 ms: 1.02x slower                                               |
| tomli_loads              | 2.17 sec                                                               | 2.21 sec: 1.02x slower                                             |
| unpickle_pure_python     | 215 us                                                                 | 219 us: 1.02x slower                                               |
| scimark_lu               | 117 ms                                                                 | 119 ms: 1.02x slower                                               |
| scimark_sparse_mat_mult  | 5.24 ms                                                                | 5.33 ms: 1.02x slower                                              |
| genshi_text              | 23.5 ms                                                                | 23.9 ms: 1.02x slower                                              |
| sqlglot_normalize        | 109 ms                                                                 | 111 ms: 1.02x slower                                               |
| xml_etree_iterparse      | 106 ms                                                                 | 108 ms: 1.02x slower                                               |
| coverage                 | 96.4 ms                                                                | 98.3 ms: 1.02x slower                                              |
| richards_super           | 53.4 ms                                                                | 54.4 ms: 1.02x slower                                              |
| unpickle                 | 15.3 us                                                                | 15.6 us: 1.02x slower                                              |
| pickle                   | 11.9 us                                                                | 12.1 us: 1.02x slower                                              |
| comprehensions           | 16.6 us                                                                | 17.0 us: 1.02x slower                                              |
| richards                 | 47.1 ms                                                                | 48.2 ms: 1.02x slower                                              |
| spectral_norm            | 113 ms                                                                 | 116 ms: 1.02x slower                                               |
| gc_traversal             | 3.77 ms                                                                | 3.87 ms: 1.03x slower                                              |
| html5lib                 | 65.7 ms                                                                | 67.4 ms: 1.03x slower                                              |
| chaos                    | 60.1 ms                                                                | 61.8 ms: 1.03x slower                                              |
| telco                    | 8.51 ms                                                                | 8.78 ms: 1.03x slower                                              |
| scimark_fft              | 370 ms                                                                 | 382 ms: 1.03x slower                                               |
| scimark_monte_carlo      | 67.7 ms                                                                | 70.6 ms: 1.04x slower                                              |
| logging_silent           | 102 ns                                                                 | 108 ns: 1.05x slower                                               |
| nbody                    | 89.4 ms                                                                | 95.5 ms: 1.07x slower                                              |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                       |

Benchmark hidden because not significant (25): async_tree_memoization_tg, django_template, async_tree_memoization, async_tree_none_tg, async_tree_none, gunicorn, aiohttp, asyncio_websockets, dask, mako, python_startup_no_site, bench_mp_pool, pycparser, async_tree_cpu_io_mixed_tg, tornado_http, xml_etree_parse, async_tree_cpu_io_mixed, json, logging_simple, async_tree_io_tg, djangocms, pprint_safe_repr, pathlib, pylint, mypy2

# HPT report

- Reliability score: 99.79% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x