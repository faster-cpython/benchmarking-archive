# Results vs. base

- fork: man-group
- ref: io_flush_full_buffer
- machine: linux-x86_64
- commit hash: 9cf294a
- commit date: 2024-03-26
- overall geometric mean: 1.00x slower
- HPT reliability: 95.66%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5+-9654daf | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 278 ms: 1.00x slower                                                        |
| chameleon      | 7.04 ms                                                                | 6.93 ms: 1.01x faster                                                       |
| html5lib       | 67.3 ms                                                                | 66.0 ms: 1.02x faster                                                       |
| tornado_http   | 96.7 ms                                                                | 96.4 ms: 1.00x faster                                                       |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_none, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5+-9654daf | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                                 | 189 ms: 1.01x faster                                                        |
| float          | 76.9 ms                                                                | 77.5 ms: 1.01x slower                                                       |
| nbody          | 91.6 ms                                                                | 93.8 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5+-9654daf | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 147 ms                                                                 | 146 ms: 1.01x faster                                                        |
| regex_effbot   | 3.67 ms                                                                | 3.69 ms: 1.01x slower                                                       |
| regex_v8       | 25.6 ms                                                                | 26.2 ms: 1.02x slower                                                       |
| regex_dna      | 219 ms                                                                 | 230 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5+-9654daf | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_dict          | 35.5 us                                                                | 33.5 us: 1.06x faster                                                       |
| pickle_list          | 5.28 us                                                                | 5.02 us: 1.05x faster                                                       |
| pickle               | 12.4 us                                                                | 11.8 us: 1.05x faster                                                       |
| json_loads           | 28.5 us                                                                | 28.3 us: 1.01x faster                                                       |
| unpickle_pure_python | 245 us                                                                 | 243 us: 1.01x faster                                                        |
| xml_etree_generate   | 87.1 ms                                                                | 86.7 ms: 1.00x faster                                                       |
| pickle_pure_python   | 307 us                                                                 | 309 us: 1.01x slower                                                        |
| xml_etree_process    | 60.5 ms                                                                | 61.0 ms: 1.01x slower                                                       |
| tomli_loads          | 2.07 sec                                                               | 2.09 sec: 1.01x slower                                                      |
| unpickle_list        | 5.04 us                                                                | 5.11 us: 1.01x slower                                                       |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                |

Benchmark hidden because not significant (4): unpickle, xml_etree_iterparse, xml_etree_parse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5+-9654daf | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.0 ms: 1.01x slower                                                       |
| python_startup_no_site | 9.41 ms                                                                | 9.50 ms: 1.01x slower                                                       |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5+-9654daf | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                       |
| genshi_text    | 25.0 ms                                                                | 25.3 ms: 1.01x slower                                                       |
| genshi_xml     | 55.3 ms                                                                | 56.3 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20240326-linux-x86_64-python-9654daf793b534b44a83-3.13.0a5+-9654daf | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_dict             | 35.5 us                                                                | 33.5 us: 1.06x faster                                                       |
| pickle_list             | 5.28 us                                                                | 5.02 us: 1.05x faster                                                       |
| pickle                  | 12.4 us                                                                | 11.8 us: 1.05x faster                                                       |
| djangocms               | 32.3 us                                                                | 31.2 us: 1.04x faster                                                       |
| coroutines              | 23.1 ms                                                                | 22.5 ms: 1.03x faster                                                       |
| html5lib                | 67.3 ms                                                                | 66.0 ms: 1.02x faster                                                       |
| spectral_norm           | 116 ms                                                                 | 114 ms: 1.02x faster                                                        |
| raytrace                | 298 ms                                                                 | 293 ms: 1.02x faster                                                        |
| chameleon               | 7.04 ms                                                                | 6.93 ms: 1.01x faster                                                       |
| fannkuch                | 402 ms                                                                 | 397 ms: 1.01x faster                                                        |
| thrift                  | 828 us                                                                 | 818 us: 1.01x faster                                                        |
| json                    | 5.35 ms                                                                | 5.29 ms: 1.01x faster                                                       |
| richards_super          | 52.8 ms                                                                | 52.3 ms: 1.01x faster                                                       |
| json_loads              | 28.5 us                                                                | 28.3 us: 1.01x faster                                                       |
| hexiom                  | 7.26 ms                                                                | 7.20 ms: 1.01x faster                                                       |
| unpickle_pure_python    | 245 us                                                                 | 243 us: 1.01x faster                                                        |
| scimark_fft             | 350 ms                                                                 | 347 ms: 1.01x faster                                                        |
| comprehensions          | 18.4 us                                                                | 18.2 us: 1.01x faster                                                       |
| scimark_sparse_mat_mult | 5.07 ms                                                                | 5.04 ms: 1.01x faster                                                       |
| regex_compile           | 147 ms                                                                 | 146 ms: 1.01x faster                                                        |
| pidigits                | 191 ms                                                                 | 189 ms: 1.01x faster                                                        |
| meteor_contest          | 111 ms                                                                 | 111 ms: 1.01x faster                                                        |
| mdp                     | 2.67 sec                                                               | 2.65 sec: 1.01x faster                                                      |
| xml_etree_generate      | 87.1 ms                                                                | 86.7 ms: 1.00x faster                                                       |
| async_generators        | 464 ms                                                                 | 462 ms: 1.00x faster                                                        |
| tornado_http            | 96.7 ms                                                                | 96.4 ms: 1.00x faster                                                       |
| asyncio_tcp_ssl         | 1.85 sec                                                               | 1.86 sec: 1.00x slower                                                      |
| sympy_integrate         | 21.7 ms                                                                | 21.8 ms: 1.00x slower                                                       |
| dulwich_log             | 70.3 ms                                                                | 70.6 ms: 1.00x slower                                                       |
| 2to3                    | 277 ms                                                                 | 278 ms: 1.00x slower                                                        |
| regex_effbot            | 3.67 ms                                                                | 3.69 ms: 1.01x slower                                                       |
| bench_thread_pool       | 854 us                                                                 | 858 us: 1.01x slower                                                        |
| go                      | 155 ms                                                                 | 156 ms: 1.01x slower                                                        |
| asyncio_tcp             | 501 ms                                                                 | 504 ms: 1.01x slower                                                        |
| deepcopy_reduce         | 3.16 us                                                                | 3.17 us: 1.01x slower                                                       |
| sympy_sum               | 164 ms                                                                 | 165 ms: 1.01x slower                                                        |
| pickle_pure_python      | 307 us                                                                 | 309 us: 1.01x slower                                                        |
| richards                | 46.1 ms                                                                | 46.4 ms: 1.01x slower                                                       |
| scimark_monte_carlo     | 70.9 ms                                                                | 71.4 ms: 1.01x slower                                                       |
| sqlglot_optimize        | 57.5 ms                                                                | 57.9 ms: 1.01x slower                                                       |
| create_gc_cycles        | 1.68 ms                                                                | 1.69 ms: 1.01x slower                                                       |
| deepcopy_memo           | 39.5 us                                                                | 39.8 us: 1.01x slower                                                       |
| sympy_str               | 290 ms                                                                 | 292 ms: 1.01x slower                                                        |
| python_startup          | 11.0 ms                                                                | 11.0 ms: 1.01x slower                                                       |
| float                   | 76.9 ms                                                                | 77.5 ms: 1.01x slower                                                       |
| xml_etree_process       | 60.5 ms                                                                | 61.0 ms: 1.01x slower                                                       |
| aiohttp                 | 1.21 ms                                                                | 1.22 ms: 1.01x slower                                                       |
| sqlglot_transpile       | 1.64 ms                                                                | 1.66 ms: 1.01x slower                                                       |
| tomli_loads             | 2.07 sec                                                               | 2.09 sec: 1.01x slower                                                      |
| sympy_expand            | 489 ms                                                                 | 494 ms: 1.01x slower                                                        |
| mako                    | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                       |
| python_startup_no_site  | 9.41 ms                                                                | 9.50 ms: 1.01x slower                                                       |
| sqlglot_normalize       | 111 ms                                                                 | 113 ms: 1.01x slower                                                        |
| scimark_lu              | 132 ms                                                                 | 133 ms: 1.01x slower                                                        |
| deepcopy                | 360 us                                                                 | 364 us: 1.01x slower                                                        |
| unpickle_list           | 5.04 us                                                                | 5.11 us: 1.01x slower                                                       |
| genshi_text             | 25.0 ms                                                                | 25.3 ms: 1.01x slower                                                       |
| logging_silent          | 101 ns                                                                 | 102 ns: 1.02x slower                                                        |
| coverage                | 97.1 ms                                                                | 98.7 ms: 1.02x slower                                                       |
| chaos                   | 63.5 ms                                                                | 64.6 ms: 1.02x slower                                                       |
| genshi_xml              | 55.3 ms                                                                | 56.3 ms: 1.02x slower                                                       |
| generators              | 29.4 ms                                                                | 30.0 ms: 1.02x slower                                                       |
| regex_v8                | 25.6 ms                                                                | 26.2 ms: 1.02x slower                                                       |
| nbody                   | 91.6 ms                                                                | 93.8 ms: 1.02x slower                                                       |
| pycparser               | 1.19 sec                                                               | 1.23 sec: 1.04x slower                                                      |
| gc_traversal            | 3.78 ms                                                                | 3.94 ms: 1.04x slower                                                       |
| regex_dna               | 219 ms                                                                 | 230 ms: 1.05x slower                                                        |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                                |

Benchmark hidden because not significant (34): pprint_pformat, crypto_pyaes, logging_format, pyflate, unpickle, sqlite_synth, xml_etree_iterparse, async_tree_cpu_io_mixed_tg, async_tree_io, bench_mp_pool, dask, async_tree_io_tg, asyncio_websockets, pprint_safe_repr, logging_simple, scimark_sor, nqueens, pylint, async_tree_memoization, mypy2, docutils, xml_etree_parse, telco, async_tree_cpu_io_mixed, gunicorn, json_dumps, pathlib, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, deltablue, django_template, sqlglot_parse, typing_runtime_protocols

# HPT report

- Reliability score: 95.66% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x