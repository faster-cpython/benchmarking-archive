# Results vs. base

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 34584c3
- commit date: 2024-04-16
- overall geometric mean: 1.00x slower
- HPT reliability: 96.74%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 270 ms                                                                 | 271 ms: 1.00x slower                                                |
| chameleon      | 7.08 ms                                                                | 6.96 ms: 1.02x faster                                               |
| html5lib       | 68.0 ms                                                                | 67.2 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_none, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 78.4 ms                                                                | 78.9 ms: 1.01x slower                                               |
| pidigits       | 191 ms                                                                 | 193 ms: 1.01x slower                                                |
| nbody          | 88.6 ms                                                                | 91.1 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 230 ms                                                                 | 222 ms: 1.03x faster                                                |
| regex_v8       | 25.5 ms                                                                | 24.9 ms: 1.02x faster                                               |
| regex_effbot   | 3.75 ms                                                                | 3.71 ms: 1.01x faster                                               |
| regex_compile  | 135 ms                                                                 | 136 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_list        | 5.19 us                                                                | 5.03 us: 1.03x faster                                               |
| json_loads           | 27.6 us                                                                | 27.8 us: 1.01x slower                                               |
| xml_etree_iterparse  | 107 ms                                                                 | 108 ms: 1.01x slower                                                |
| pickle_pure_python   | 298 us                                                                 | 302 us: 1.01x slower                                                |
| xml_etree_generate   | 87.6 ms                                                                | 88.7 ms: 1.01x slower                                               |
| pickle               | 11.9 us                                                                | 12.0 us: 1.01x slower                                               |
| xml_etree_process    | 59.9 ms                                                                | 60.8 ms: 1.02x slower                                               |
| tomli_loads          | 2.17 sec                                                               | 2.21 sec: 1.02x slower                                              |
| unpickle_pure_python | 216 us                                                                 | 220 us: 1.02x slower                                                |
| pickle_dict          | 34.5 us                                                                | 35.4 us: 1.03x slower                                               |
| pickle_list          | 5.00 us                                                                | 5.40 us: 1.08x slower                                               |
| unpickle             | 15.7 us                                                                | 17.0 us: 1.08x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                        |

Benchmark hidden because not significant (2): json_dumps, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                               |
| python_startup_no_site | 7.08 ms                                                                | 7.13 ms: 1.01x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako           | 10.8 ms                                                                | 11.0 ms: 1.01x slower                                               |
| genshi_xml     | 52.1 ms                                                                | 52.9 ms: 1.01x slower                                               |
| genshi_text    | 23.4 ms                                                                | 23.9 ms: 1.02x slower                                               |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                        |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                | bm-20240416-linux-x86_64-python-acf69e09c66f8473399f-3.13.0a6+-acf69e0 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|--------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pycparser                | 1.21 sec                                                               | 1.16 sec: 1.04x faster                                              |
| regex_dna                | 230 ms                                                                 | 222 ms: 1.03x faster                                                |
| unpickle_list            | 5.19 us                                                                | 5.03 us: 1.03x faster                                               |
| coverage                 | 99.7 ms                                                                | 96.8 ms: 1.03x faster                                               |
| mdp                      | 2.67 sec                                                               | 2.59 sec: 1.03x faster                                              |
| async_generators         | 453 ms                                                                 | 443 ms: 1.02x faster                                                |
| regex_v8                 | 25.5 ms                                                                | 24.9 ms: 1.02x faster                                               |
| generators               | 30.3 ms                                                                | 29.7 ms: 1.02x faster                                               |
| chameleon                | 7.08 ms                                                                | 6.96 ms: 1.02x faster                                               |
| gc_traversal             | 4.02 ms                                                                | 3.96 ms: 1.01x faster                                               |
| html5lib                 | 68.0 ms                                                                | 67.2 ms: 1.01x faster                                               |
| regex_effbot             | 3.75 ms                                                                | 3.71 ms: 1.01x faster                                               |
| scimark_sor              | 123 ms                                                                 | 122 ms: 1.01x faster                                                |
| fannkuch                 | 391 ms                                                                 | 387 ms: 1.01x faster                                                |
| thrift                   | 830 us                                                                 | 823 us: 1.01x faster                                                |
| crypto_pyaes             | 75.3 ms                                                                | 74.7 ms: 1.01x faster                                               |
| deepcopy                 | 356 us                                                                 | 354 us: 1.01x faster                                                |
| scimark_lu               | 116 ms                                                                 | 115 ms: 1.01x faster                                                |
| sympy_expand             | 475 ms                                                                 | 473 ms: 1.00x faster                                                |
| asyncio_tcp_ssl          | 1.84 sec                                                               | 1.84 sec: 1.00x faster                                              |
| 2to3                     | 270 ms                                                                 | 271 ms: 1.00x slower                                                |
| sqlglot_optimize         | 55.5 ms                                                                | 55.6 ms: 1.00x slower                                               |
| sympy_integrate          | 20.4 ms                                                                | 20.5 ms: 1.00x slower                                               |
| python_startup           | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                               |
| pyflate                  | 464 ms                                                                 | 467 ms: 1.01x slower                                                |
| go                       | 143 ms                                                                 | 143 ms: 1.01x slower                                                |
| logging_simple           | 5.75 us                                                                | 5.78 us: 1.01x slower                                               |
| sqlglot_normalize        | 111 ms                                                                 | 111 ms: 1.01x slower                                                |
| raytrace                 | 261 ms                                                                 | 263 ms: 1.01x slower                                                |
| python_startup_no_site   | 7.08 ms                                                                | 7.13 ms: 1.01x slower                                               |
| dulwich_log              | 66.2 ms                                                                | 66.7 ms: 1.01x slower                                               |
| float                    | 78.4 ms                                                                | 78.9 ms: 1.01x slower                                               |
| hexiom                   | 6.33 ms                                                                | 6.37 ms: 1.01x slower                                               |
| json_loads               | 27.6 us                                                                | 27.8 us: 1.01x slower                                               |
| comprehensions           | 16.9 us                                                                | 17.1 us: 1.01x slower                                               |
| regex_compile            | 135 ms                                                                 | 136 ms: 1.01x slower                                                |
| sqlglot_transpile        | 1.58 ms                                                                | 1.60 ms: 1.01x slower                                               |
| telco                    | 8.56 ms                                                                | 8.65 ms: 1.01x slower                                               |
| deepcopy_memo            | 37.9 us                                                                | 38.3 us: 1.01x slower                                               |
| sqlglot_parse            | 1.28 ms                                                                | 1.29 ms: 1.01x slower                                               |
| pidigits                 | 191 ms                                                                 | 193 ms: 1.01x slower                                                |
| xml_etree_iterparse      | 107 ms                                                                 | 108 ms: 1.01x slower                                                |
| scimark_fft              | 365 ms                                                                 | 370 ms: 1.01x slower                                                |
| pickle_pure_python       | 298 us                                                                 | 302 us: 1.01x slower                                                |
| xml_etree_generate       | 87.6 ms                                                                | 88.7 ms: 1.01x slower                                               |
| pickle                   | 11.9 us                                                                | 12.0 us: 1.01x slower                                               |
| mako                     | 10.8 ms                                                                | 11.0 ms: 1.01x slower                                               |
| pprint_safe_repr         | 743 ms                                                                 | 754 ms: 1.01x slower                                                |
| genshi_xml               | 52.1 ms                                                                | 52.9 ms: 1.01x slower                                               |
| xml_etree_process        | 59.9 ms                                                                | 60.8 ms: 1.02x slower                                               |
| richards                 | 47.7 ms                                                                | 48.4 ms: 1.02x slower                                               |
| richards_super           | 53.5 ms                                                                | 54.4 ms: 1.02x slower                                               |
| meteor_contest           | 110 ms                                                                 | 111 ms: 1.02x slower                                                |
| pprint_pformat           | 1.52 sec                                                               | 1.55 sec: 1.02x slower                                              |
| spectral_norm            | 111 ms                                                                 | 113 ms: 1.02x slower                                                |
| json                     | 5.15 ms                                                                | 5.25 ms: 1.02x slower                                               |
| scimark_monte_carlo      | 67.1 ms                                                                | 68.5 ms: 1.02x slower                                               |
| tomli_loads              | 2.17 sec                                                               | 2.21 sec: 1.02x slower                                              |
| unpickle_pure_python     | 216 us                                                                 | 220 us: 1.02x slower                                                |
| genshi_text              | 23.4 ms                                                                | 23.9 ms: 1.02x slower                                               |
| typing_runtime_protocols | 113 us                                                                 | 116 us: 1.03x slower                                                |
| deltablue                | 3.20 ms                                                                | 3.29 ms: 1.03x slower                                               |
| nbody                    | 88.6 ms                                                                | 91.1 ms: 1.03x slower                                               |
| pickle_dict              | 34.5 us                                                                | 35.4 us: 1.03x slower                                               |
| pickle_list              | 5.00 us                                                                | 5.40 us: 1.08x slower                                               |
| unpickle                 | 15.7 us                                                                | 17.0 us: 1.08x slower                                               |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (35): async_tree_memoization, dask, async_tree_io_tg, sqlite_synth, chaos, async_tree_cpu_io_mixed_tg, logging_silent, scimark_sparse_mat_mult, deepcopy_reduce, async_tree_none_tg, bench_thread_pool, tornado_http, create_gc_cycles, docutils, async_tree_cpu_io_mixed, nqueens, bench_mp_pool, asyncio_tcp, pathlib, django_template, asyncio_websockets, async_tree_memoization_tg, sympy_str, pylint, sympy_sum, aiohttp, coroutines, json_dumps, logging_format, gunicorn, djangocms, xml_etree_parse, mypy2, async_tree_none, async_tree_io

# HPT report

- Reliability score: 96.74% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x