# Results vs. base

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 5e20f0f
- commit date: 2024-04-17
- overall geometric mean: 1.00x faster
- HPT reliability: 69.25%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 270 ms                                                                 | 269 ms: 1.01x faster                                                |
| docutils       | 2.83 sec                                                               | 2.82 sec: 1.00x faster                                              |
| html5lib       | 68.0 ms                                                                | 65.8 ms: 1.03x faster                                               |
| tornado_http   | 94.4 ms                                                                | 93.9 ms: 1.00x faster                                               |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io  | 913 ms                                                                 | 943 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (7): async_tree_memoization, async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 88.6 ms                                                                | 87.2 ms: 1.02x faster                                               |
| pidigits       | 191 ms                                                                 | 190 ms: 1.00x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 230 ms                                                                 | 225 ms: 1.02x faster                                                |
| regex_v8       | 25.5 ms                                                                | 25.0 ms: 1.02x faster                                               |
| regex_effbot   | 3.75 ms                                                                | 3.73 ms: 1.00x faster                                               |
| regex_compile  | 135 ms                                                                 | 134 ms: 1.00x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_list        | 5.19 us                                                                | 5.03 us: 1.03x faster                                               |
| unpickle_pure_python | 216 us                                                                 | 214 us: 1.01x faster                                                |
| pickle_dict          | 34.5 us                                                                | 34.3 us: 1.01x faster                                               |
| json_dumps           | 10.6 ms                                                                | 10.5 ms: 1.00x faster                                               |
| xml_etree_generate   | 87.6 ms                                                                | 87.8 ms: 1.00x slower                                               |
| json_loads           | 27.6 us                                                                | 27.7 us: 1.00x slower                                               |
| pickle_pure_python   | 298 us                                                                 | 302 us: 1.01x slower                                                |
| xml_etree_process    | 59.9 ms                                                                | 60.9 ms: 1.02x slower                                               |
| pickle_list          | 5.00 us                                                                | 5.13 us: 1.03x slower                                               |
| unpickle             | 15.7 us                                                                | 16.6 us: 1.06x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                        |

Benchmark hidden because not significant (4): tomli_loads, xml_etree_parse, pickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                                | 51.4 ms: 1.01x faster                                               |
| mako            | 10.8 ms                                                                | 10.7 ms: 1.01x faster                                               |
| genshi_text     | 23.4 ms                                                                | 23.3 ms: 1.01x faster                                               |
| django_template | 35.0 ms                                                                | 35.5 ms: 1.01x slower                                               |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                        |

All benchmarks:
===============

| Benchmark            | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal         | 4.02 ms                                                                | 3.68 ms: 1.09x faster                                               |
| pycparser            | 1.21 sec                                                               | 1.16 sec: 1.04x faster                                              |
| html5lib             | 68.0 ms                                                                | 65.8 ms: 1.03x faster                                               |
| unpickle_list        | 5.19 us                                                                | 5.03 us: 1.03x faster                                               |
| hexiom               | 6.33 ms                                                                | 6.14 ms: 1.03x faster                                               |
| crypto_pyaes         | 75.3 ms                                                                | 73.5 ms: 1.02x faster                                               |
| deepcopy_memo        | 37.9 us                                                                | 37.0 us: 1.02x faster                                               |
| regex_dna            | 230 ms                                                                 | 225 ms: 1.02x faster                                                |
| generators           | 30.3 ms                                                                | 29.7 ms: 1.02x faster                                               |
| regex_v8             | 25.5 ms                                                                | 25.0 ms: 1.02x faster                                               |
| thrift               | 830 us                                                                 | 816 us: 1.02x faster                                                |
| coverage             | 99.7 ms                                                                | 98.0 ms: 1.02x faster                                               |
| logging_silent       | 102 ns                                                                 | 101 ns: 1.02x faster                                                |
| nbody                | 88.6 ms                                                                | 87.2 ms: 1.02x faster                                               |
| genshi_xml           | 52.1 ms                                                                | 51.4 ms: 1.01x faster                                               |
| richards_super       | 53.5 ms                                                                | 52.7 ms: 1.01x faster                                               |
| async_generators     | 453 ms                                                                 | 447 ms: 1.01x faster                                                |
| mako                 | 10.8 ms                                                                | 10.7 ms: 1.01x faster                                               |
| coroutines           | 22.9 ms                                                                | 22.7 ms: 1.01x faster                                               |
| richards             | 47.7 ms                                                                | 47.3 ms: 1.01x faster                                               |
| go                   | 143 ms                                                                 | 141 ms: 1.01x faster                                                |
| create_gc_cycles     | 1.75 ms                                                                | 1.74 ms: 1.01x faster                                               |
| comprehensions       | 16.9 us                                                                | 16.8 us: 1.01x faster                                               |
| unpickle_pure_python | 216 us                                                                 | 214 us: 1.01x faster                                                |
| 2to3                 | 270 ms                                                                 | 269 ms: 1.01x faster                                                |
| scimark_sor          | 123 ms                                                                 | 123 ms: 1.01x faster                                                |
| pickle_dict          | 34.5 us                                                                | 34.3 us: 1.01x faster                                               |
| genshi_text          | 23.4 ms                                                                | 23.3 ms: 1.01x faster                                               |
| regex_effbot         | 3.75 ms                                                                | 3.73 ms: 1.00x faster                                               |
| tornado_http         | 94.4 ms                                                                | 93.9 ms: 1.00x faster                                               |
| docutils             | 2.83 sec                                                               | 2.82 sec: 1.00x faster                                              |
| meteor_contest       | 110 ms                                                                 | 109 ms: 1.00x faster                                                |
| json_dumps           | 10.6 ms                                                                | 10.5 ms: 1.00x faster                                               |
| regex_compile        | 135 ms                                                                 | 134 ms: 1.00x faster                                                |
| bench_thread_pool    | 839 us                                                                 | 836 us: 1.00x faster                                                |
| sqlglot_optimize     | 55.5 ms                                                                | 55.3 ms: 1.00x faster                                               |
| pidigits             | 191 ms                                                                 | 190 ms: 1.00x faster                                                |
| asyncio_tcp_ssl      | 1.84 sec                                                               | 1.84 sec: 1.00x faster                                              |
| sympy_integrate      | 20.4 ms                                                                | 20.4 ms: 1.00x slower                                               |
| xml_etree_generate   | 87.6 ms                                                                | 87.8 ms: 1.00x slower                                               |
| mdp                  | 2.67 sec                                                               | 2.68 sec: 1.00x slower                                              |
| nqueens              | 81.5 ms                                                                | 81.9 ms: 1.00x slower                                               |
| json_loads           | 27.6 us                                                                | 27.7 us: 1.00x slower                                               |
| fannkuch             | 391 ms                                                                 | 394 ms: 1.01x slower                                                |
| sqlite_synth         | 2.96 us                                                                | 2.98 us: 1.01x slower                                               |
| pprint_pformat       | 1.52 sec                                                               | 1.54 sec: 1.01x slower                                              |
| raytrace             | 261 ms                                                                 | 264 ms: 1.01x slower                                                |
| deepcopy_reduce      | 3.18 us                                                                | 3.22 us: 1.01x slower                                               |
| asyncio_websockets   | 562 ms                                                                 | 569 ms: 1.01x slower                                                |
| django_template      | 35.0 ms                                                                | 35.5 ms: 1.01x slower                                               |
| pickle_pure_python   | 298 us                                                                 | 302 us: 1.01x slower                                                |
| scimark_monte_carlo  | 67.1 ms                                                                | 68.2 ms: 1.02x slower                                               |
| pathlib              | 17.5 ms                                                                | 17.8 ms: 1.02x slower                                               |
| xml_etree_process    | 59.9 ms                                                                | 60.9 ms: 1.02x slower                                               |
| telco                | 8.56 ms                                                                | 8.71 ms: 1.02x slower                                               |
| logging_format       | 6.39 us                                                                | 6.50 us: 1.02x slower                                               |
| pprint_safe_repr     | 743 ms                                                                 | 756 ms: 1.02x slower                                                |
| logging_simple       | 5.75 us                                                                | 5.85 us: 1.02x slower                                               |
| pickle_list          | 5.00 us                                                                | 5.13 us: 1.03x slower                                               |
| async_tree_io        | 913 ms                                                                 | 943 ms: 1.03x slower                                                |
| scimark_fft          | 365 ms                                                                 | 378 ms: 1.04x slower                                                |
| spectral_norm        | 111 ms                                                                 | 115 ms: 1.04x slower                                                |
| unpickle             | 15.7 us                                                                | 16.6 us: 1.06x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (38): async_tree_memoization, async_tree_io_tg, dask, djangocms, scimark_lu, dulwich_log, scimark_sparse_mat_mult, async_tree_none_tg, sqlglot_transpile, asyncio_tcp, float, pylint, python_startup, aiohttp, sympy_expand, deepcopy, async_tree_memoization_tg, python_startup_no_site, sqlglot_parse, chaos, sqlglot_normalize, pyflate, tomli_loads, xml_etree_parse, mypy2, pickle, deltablue, gunicorn, async_tree_cpu_io_mixed_tg, xml_etree_iterparse, sympy_str, chameleon, bench_mp_pool, sympy_sum, typing_runtime_protocols, async_tree_cpu_io_mixed, json, async_tree_none

# HPT report

- Reliability score: 69.25% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x