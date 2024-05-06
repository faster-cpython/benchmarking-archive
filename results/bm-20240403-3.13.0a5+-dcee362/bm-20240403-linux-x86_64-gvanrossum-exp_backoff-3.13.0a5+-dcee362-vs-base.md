# Results vs. base

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: dcee362
- commit date: 2024-04-03
- overall geometric mean: 1.00x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 269 ms                                                                 | 270 ms: 1.00x slower                                              |
| chameleon      | 6.86 ms                                                                | 6.92 ms: 1.01x slower                                             |
| docutils       | 2.80 sec                                                               | 2.82 sec: 1.01x slower                                            |
| html5lib       | 67.5 ms                                                                | 68.2 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_io, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 197 ms                                                                 | 194 ms: 1.02x faster                                              |
| float          | 77.6 ms                                                                | 79.2 ms: 1.02x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 26.0 ms                                                                | 25.5 ms: 1.02x faster                                             |
| regex_effbot   | 3.77 ms                                                                | 3.72 ms: 1.01x faster                                             |
| regex_compile  | 134 ms                                                                 | 135 ms: 1.01x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_dict          | 34.3 us                                                                | 32.9 us: 1.04x faster                                             |
| pickle_list          | 4.95 us                                                                | 4.79 us: 1.03x faster                                             |
| unpickle_list        | 5.10 us                                                                | 5.02 us: 1.02x faster                                             |
| tomli_loads          | 2.19 sec                                                               | 2.16 sec: 1.01x faster                                            |
| json_loads           | 28.7 us                                                                | 28.5 us: 1.01x faster                                             |
| unpickle             | 15.1 us                                                                | 14.9 us: 1.01x faster                                             |
| pickle               | 11.7 us                                                                | 11.6 us: 1.01x faster                                             |
| xml_etree_process    | 59.9 ms                                                                | 60.4 ms: 1.01x slower                                             |
| xml_etree_generate   | 87.0 ms                                                                | 87.9 ms: 1.01x slower                                             |
| pickle_pure_python   | 297 us                                                                 | 303 us: 1.02x slower                                              |
| unpickle_pure_python | 217 us                                                                 | 226 us: 1.04x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (3): json_dumps, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 10.6 ms                                                                | 10.5 ms: 1.00x faster                                             |
| python_startup_no_site | 9.00 ms                                                                | 8.98 ms: 1.00x faster                                             |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako           | 11.0 ms                                                                | 10.7 ms: 1.02x faster                                             |
| genshi_xml     | 51.2 ms                                                                | 52.1 ms: 1.02x slower                                             |
| genshi_text    | 23.4 ms                                                                | 24.0 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

All benchmarks:
===============

| Benchmark               | bm-20240403-linux-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|-------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_dict             | 34.3 us                                                                | 32.9 us: 1.04x faster                                             |
| pickle_list             | 4.95 us                                                                | 4.79 us: 1.03x faster                                             |
| deepcopy_memo           | 38.9 us                                                                | 37.9 us: 1.03x faster                                             |
| pycparser               | 1.19 sec                                                               | 1.16 sec: 1.02x faster                                            |
| mako                    | 11.0 ms                                                                | 10.7 ms: 1.02x faster                                             |
| coroutines              | 22.7 ms                                                                | 22.2 ms: 1.02x faster                                             |
| regex_v8                | 26.0 ms                                                                | 25.5 ms: 1.02x faster                                             |
| pidigits                | 197 ms                                                                 | 194 ms: 1.02x faster                                              |
| create_gc_cycles        | 1.75 ms                                                                | 1.73 ms: 1.02x faster                                             |
| unpickle_list           | 5.10 us                                                                | 5.02 us: 1.02x faster                                             |
| regex_effbot            | 3.77 ms                                                                | 3.72 ms: 1.01x faster                                             |
| tomli_loads             | 2.19 sec                                                               | 2.16 sec: 1.01x faster                                            |
| logging_format          | 6.42 us                                                                | 6.36 us: 1.01x faster                                             |
| json_loads              | 28.7 us                                                                | 28.5 us: 1.01x faster                                             |
| unpickle                | 15.1 us                                                                | 14.9 us: 1.01x faster                                             |
| pickle                  | 11.7 us                                                                | 11.6 us: 1.01x faster                                             |
| go                      | 143 ms                                                                 | 142 ms: 1.01x faster                                              |
| pyflate                 | 468 ms                                                                 | 465 ms: 1.01x faster                                              |
| dulwich_log             | 67.7 ms                                                                | 67.3 ms: 1.01x faster                                             |
| logging_simple          | 5.79 us                                                                | 5.76 us: 1.01x faster                                             |
| coverage                | 96.8 ms                                                                | 96.2 ms: 1.01x faster                                             |
| comprehensions          | 16.6 us                                                                | 16.5 us: 1.01x faster                                             |
| sqlglot_normalize       | 111 ms                                                                 | 110 ms: 1.00x faster                                              |
| python_startup          | 10.6 ms                                                                | 10.5 ms: 1.00x faster                                             |
| python_startup_no_site  | 9.00 ms                                                                | 8.98 ms: 1.00x faster                                             |
| logging_silent          | 99.1 ns                                                                | 99.5 ns: 1.00x slower                                             |
| 2to3                    | 269 ms                                                                 | 270 ms: 1.00x slower                                              |
| sympy_integrate         | 20.3 ms                                                                | 20.4 ms: 1.00x slower                                             |
| sympy_sum               | 155 ms                                                                 | 156 ms: 1.00x slower                                              |
| sqlglot_optimize        | 54.9 ms                                                                | 55.2 ms: 1.00x slower                                             |
| xml_etree_process       | 59.9 ms                                                                | 60.4 ms: 1.01x slower                                             |
| sympy_expand            | 466 ms                                                                 | 470 ms: 1.01x slower                                              |
| gc_traversal            | 3.94 ms                                                                | 3.97 ms: 1.01x slower                                             |
| chameleon               | 6.86 ms                                                                | 6.92 ms: 1.01x slower                                             |
| docutils                | 2.80 sec                                                               | 2.82 sec: 1.01x slower                                            |
| pylint                  | 278 ms                                                                 | 281 ms: 1.01x slower                                              |
| sympy_str               | 277 ms                                                                 | 279 ms: 1.01x slower                                              |
| fannkuch                | 392 ms                                                                 | 396 ms: 1.01x slower                                              |
| deepcopy                | 356 us                                                                 | 359 us: 1.01x slower                                              |
| sqlglot_transpile       | 1.58 ms                                                                | 1.60 ms: 1.01x slower                                             |
| html5lib                | 67.5 ms                                                                | 68.2 ms: 1.01x slower                                             |
| xml_etree_generate      | 87.0 ms                                                                | 87.9 ms: 1.01x slower                                             |
| meteor_contest          | 108 ms                                                                 | 110 ms: 1.01x slower                                              |
| bench_thread_pool       | 825 us                                                                 | 833 us: 1.01x slower                                              |
| regex_compile           | 134 ms                                                                 | 135 ms: 1.01x slower                                              |
| chaos                   | 60.3 ms                                                                | 60.9 ms: 1.01x slower                                             |
| hexiom                  | 6.21 ms                                                                | 6.28 ms: 1.01x slower                                             |
| generators              | 29.6 ms                                                                | 30.0 ms: 1.01x slower                                             |
| sqlglot_parse           | 1.27 ms                                                                | 1.29 ms: 1.01x slower                                             |
| richards_super          | 52.3 ms                                                                | 53.1 ms: 1.02x slower                                             |
| async_generators        | 438 ms                                                                 | 445 ms: 1.02x slower                                              |
| pathlib                 | 18.8 ms                                                                | 19.1 ms: 1.02x slower                                             |
| raytrace                | 260 ms                                                                 | 264 ms: 1.02x slower                                              |
| richards                | 46.2 ms                                                                | 47.0 ms: 1.02x slower                                             |
| genshi_xml              | 51.2 ms                                                                | 52.1 ms: 1.02x slower                                             |
| sqlite_synth            | 2.90 us                                                                | 2.95 us: 1.02x slower                                             |
| pickle_pure_python      | 297 us                                                                 | 303 us: 1.02x slower                                              |
| spectral_norm           | 110 ms                                                                 | 112 ms: 1.02x slower                                              |
| scimark_lu              | 112 ms                                                                 | 114 ms: 1.02x slower                                              |
| nqueens                 | 82.0 ms                                                                | 83.5 ms: 1.02x slower                                             |
| scimark_monte_carlo     | 67.6 ms                                                                | 68.9 ms: 1.02x slower                                             |
| deepcopy_reduce         | 3.16 us                                                                | 3.22 us: 1.02x slower                                             |
| float                   | 77.6 ms                                                                | 79.2 ms: 1.02x slower                                             |
| pprint_pformat          | 1.50 sec                                                               | 1.53 sec: 1.02x slower                                            |
| pprint_safe_repr        | 734 ms                                                                 | 751 ms: 1.02x slower                                              |
| genshi_text             | 23.4 ms                                                                | 24.0 ms: 1.03x slower                                             |
| telco                   | 8.38 ms                                                                | 8.65 ms: 1.03x slower                                             |
| scimark_sparse_mat_mult | 4.99 ms                                                                | 5.15 ms: 1.03x slower                                             |
| mdp                     | 2.55 sec                                                               | 2.65 sec: 1.04x slower                                            |
| unpickle_pure_python    | 217 us                                                                 | 226 us: 1.04x slower                                              |
| crypto_pyaes            | 72.7 ms                                                                | 76.3 ms: 1.05x slower                                             |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (28): async_tree_io_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, json_dumps, thrift, async_tree_none_tg, xml_etree_parse, gunicorn, asyncio_tcp, regex_dna, asyncio_websockets, asyncio_tcp_ssl, bench_mp_pool, async_tree_io, mypy2, scimark_sor, tornado_http, async_tree_memoization_tg, nbody, async_tree_cpu_io_mixed, aiohttp, deltablue, xml_etree_iterparse, typing_runtime_protocols, dask, json, async_tree_none, scimark_fft

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x