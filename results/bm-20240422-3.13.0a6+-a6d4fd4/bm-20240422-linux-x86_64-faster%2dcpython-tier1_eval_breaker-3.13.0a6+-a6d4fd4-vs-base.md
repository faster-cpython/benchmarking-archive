# Results vs. base

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: linux-x86_64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.01x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240422-linux-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 270 ms                                                                 | 273 ms: 1.01x slower                                                           |
| chameleon      | 6.92 ms                                                                | 7.17 ms: 1.04x slower                                                          |
| html5lib       | 68.2 ms                                                                | 66.5 ms: 1.02x faster                                                          |
| tornado_http   | 94.1 ms                                                                | 94.7 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                   |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240422-linux-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pidigits       | 197 ms                                                                 | 193 ms: 1.02x faster                                                           |
| nbody          | 88.5 ms                                                                | 92.6 ms: 1.05x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                   |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240422-linux-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_v8       | 28.8 ms                                                                | 25.8 ms: 1.12x faster                                                          |
| regex_compile  | 135 ms                                                                 | 137 ms: 1.01x slower                                                           |
| regex_dna      | 228 ms                                                                 | 233 ms: 1.02x slower                                                           |
| regex_effbot   | 3.75 ms                                                                | 3.83 ms: 1.02x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240422-linux-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pickle_dict          | 35.3 us                                                                | 35.4 us: 1.00x slower                                                          |
| pickle_list          | 5.18 us                                                                | 5.21 us: 1.01x slower                                                          |
| unpickle_list        | 5.30 us                                                                | 5.35 us: 1.01x slower                                                          |
| xml_etree_process    | 60.4 ms                                                                | 61.2 ms: 1.01x slower                                                          |
| pickle_pure_python   | 303 us                                                                 | 308 us: 1.02x slower                                                           |
| xml_etree_generate   | 86.9 ms                                                                | 88.6 ms: 1.02x slower                                                          |
| unpickle_pure_python | 218 us                                                                 | 224 us: 1.03x slower                                                           |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                                   |

Benchmark hidden because not significant (7): json_dumps, unpickle, json_loads, xml_etree_iterparse, pickle, tomli_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240422-linux-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x slower                                                          |
| python_startup_no_site | 7.07 ms                                                                | 7.11 ms: 1.01x slower                                                          |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240422-linux-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| genshi_xml     | 51.8 ms                                                                | 52.2 ms: 1.01x slower                                                          |
| genshi_text    | 23.6 ms                                                                | 24.0 ms: 1.02x slower                                                          |
| mako           | 11.0 ms                                                                | 11.3 ms: 1.02x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                   |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                | bm-20240422-linux-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|--------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_v8                 | 28.8 ms                                                                | 25.8 ms: 1.12x faster                                                          |
| scimark_sor              | 131 ms                                                                 | 123 ms: 1.07x faster                                                           |
| thrift                   | 827 us                                                                 | 804 us: 1.03x faster                                                           |
| html5lib                 | 68.2 ms                                                                | 66.5 ms: 1.02x faster                                                          |
| pidigits                 | 197 ms                                                                 | 193 ms: 1.02x faster                                                           |
| deepcopy_reduce          | 3.22 us                                                                | 3.18 us: 1.01x faster                                                          |
| richards                 | 47.2 ms                                                                | 46.9 ms: 1.01x faster                                                          |
| sympy_sum                | 157 ms                                                                 | 156 ms: 1.01x faster                                                           |
| coroutines               | 22.6 ms                                                                | 22.5 ms: 1.00x faster                                                          |
| asyncio_tcp_ssl          | 1.84 sec                                                               | 1.85 sec: 1.00x slower                                                         |
| pickle_dict              | 35.3 us                                                                | 35.4 us: 1.00x slower                                                          |
| python_startup           | 10.5 ms                                                                | 10.5 ms: 1.00x slower                                                          |
| sympy_integrate          | 20.3 ms                                                                | 20.4 ms: 1.00x slower                                                          |
| python_startup_no_site   | 7.07 ms                                                                | 7.11 ms: 1.01x slower                                                          |
| asyncio_tcp              | 508 ms                                                                 | 511 ms: 1.01x slower                                                           |
| pickle_list              | 5.18 us                                                                | 5.21 us: 1.01x slower                                                          |
| sqlite_synth             | 2.95 us                                                                | 2.97 us: 1.01x slower                                                          |
| tornado_http             | 94.1 ms                                                                | 94.7 ms: 1.01x slower                                                          |
| bench_thread_pool        | 831 us                                                                 | 836 us: 1.01x slower                                                           |
| genshi_xml               | 51.8 ms                                                                | 52.2 ms: 1.01x slower                                                          |
| richards_super           | 53.0 ms                                                                | 53.3 ms: 1.01x slower                                                          |
| pprint_pformat           | 1.55 sec                                                               | 1.56 sec: 1.01x slower                                                         |
| unpickle_list            | 5.30 us                                                                | 5.35 us: 1.01x slower                                                          |
| sqlglot_parse            | 1.28 ms                                                                | 1.29 ms: 1.01x slower                                                          |
| sqlglot_optimize         | 55.0 ms                                                                | 55.6 ms: 1.01x slower                                                          |
| logging_format           | 6.41 us                                                                | 6.48 us: 1.01x slower                                                          |
| sqlglot_transpile        | 1.59 ms                                                                | 1.60 ms: 1.01x slower                                                          |
| pprint_safe_repr         | 751 ms                                                                 | 760 ms: 1.01x slower                                                           |
| xml_etree_process        | 60.4 ms                                                                | 61.2 ms: 1.01x slower                                                          |
| 2to3                     | 270 ms                                                                 | 273 ms: 1.01x slower                                                           |
| sympy_expand             | 471 ms                                                                 | 477 ms: 1.01x slower                                                           |
| dulwich_log              | 65.9 ms                                                                | 66.8 ms: 1.01x slower                                                          |
| regex_compile            | 135 ms                                                                 | 137 ms: 1.01x slower                                                           |
| scimark_fft              | 374 ms                                                                 | 379 ms: 1.01x slower                                                           |
| scimark_monte_carlo      | 67.7 ms                                                                | 68.8 ms: 1.02x slower                                                          |
| pickle_pure_python       | 303 us                                                                 | 308 us: 1.02x slower                                                           |
| pyflate                  | 487 ms                                                                 | 495 ms: 1.02x slower                                                           |
| deepcopy                 | 354 us                                                                 | 360 us: 1.02x slower                                                           |
| genshi_text              | 23.6 ms                                                                | 24.0 ms: 1.02x slower                                                          |
| chaos                    | 60.0 ms                                                                | 61.0 ms: 1.02x slower                                                          |
| generators               | 29.8 ms                                                                | 30.3 ms: 1.02x slower                                                          |
| crypto_pyaes             | 75.0 ms                                                                | 76.3 ms: 1.02x slower                                                          |
| logging_silent           | 99.7 ns                                                                | 102 ns: 1.02x slower                                                           |
| async_generators         | 442 ms                                                                 | 451 ms: 1.02x slower                                                           |
| xml_etree_generate       | 86.9 ms                                                                | 88.6 ms: 1.02x slower                                                          |
| create_gc_cycles         | 1.74 ms                                                                | 1.77 ms: 1.02x slower                                                          |
| regex_dna                | 228 ms                                                                 | 233 ms: 1.02x slower                                                           |
| regex_effbot             | 3.75 ms                                                                | 3.83 ms: 1.02x slower                                                          |
| meteor_contest           | 110 ms                                                                 | 112 ms: 1.02x slower                                                           |
| coverage                 | 96.7 ms                                                                | 98.8 ms: 1.02x slower                                                          |
| mako                     | 11.0 ms                                                                | 11.3 ms: 1.02x slower                                                          |
| fannkuch                 | 397 ms                                                                 | 406 ms: 1.02x slower                                                           |
| nqueens                  | 79.9 ms                                                                | 81.9 ms: 1.02x slower                                                          |
| comprehensions           | 16.9 us                                                                | 17.3 us: 1.03x slower                                                          |
| typing_runtime_protocols | 113 us                                                                 | 116 us: 1.03x slower                                                           |
| unpickle_pure_python     | 218 us                                                                 | 224 us: 1.03x slower                                                           |
| scimark_sparse_mat_mult  | 5.18 ms                                                                | 5.33 ms: 1.03x slower                                                          |
| deltablue                | 3.22 ms                                                                | 3.34 ms: 1.04x slower                                                          |
| chameleon                | 6.92 ms                                                                | 7.17 ms: 1.04x slower                                                          |
| hexiom                   | 6.20 ms                                                                | 6.45 ms: 1.04x slower                                                          |
| nbody                    | 88.5 ms                                                                | 92.6 ms: 1.05x slower                                                          |
| deepcopy_memo            | 37.4 us                                                                | 39.4 us: 1.05x slower                                                          |
| spectral_norm            | 111 ms                                                                 | 117 ms: 1.05x slower                                                           |
| gc_traversal             | 3.76 ms                                                                | 3.98 ms: 1.06x slower                                                          |
| pycparser                | 1.14 sec                                                               | 1.22 sec: 1.07x slower                                                         |
| mdp                      | 2.59 sec                                                               | 2.79 sec: 1.08x slower                                                         |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                                   |

Benchmark hidden because not significant (35): async_tree_memoization_tg, json_dumps, async_tree_none_tg, djangocms, logging_simple, unpickle, json_loads, pathlib, raytrace, xml_etree_iterparse, asyncio_websockets, django_template, bench_mp_pool, sqlglot_normalize, float, gunicorn, go, docutils, aiohttp, async_tree_cpu_io_mixed, scimark_lu, pickle, tomli_loads, async_tree_io_tg, json, async_tree_cpu_io_mixed_tg, dask, xml_etree_parse, telco, sympy_str, pylint, mypy2, async_tree_io, async_tree_none, async_tree_memoization

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x