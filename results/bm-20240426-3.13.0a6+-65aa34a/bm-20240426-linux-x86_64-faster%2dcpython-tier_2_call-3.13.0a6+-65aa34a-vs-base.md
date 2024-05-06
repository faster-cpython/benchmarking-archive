# Results vs. base

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.00x faster
- HPT reliability: 98.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 269 ms                                                                 | 267 ms: 1.01x faster                                                    |
| docutils       | 2.81 sec                                                               | 2.80 sec: 1.00x faster                                                  |
| html5lib       | 67.9 ms                                                                | 65.6 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (2): chameleon, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none_tg, async_tree_io, async_tree_memoization_tg, async_tree_io_tg, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 215 ms                                                                 | 194 ms: 1.11x faster                                                    |
| nbody          | 89.9 ms                                                                | 87.4 ms: 1.03x faster                                                   |
| float          | 78.0 ms                                                                | 78.8 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.90 ms                                                                | 3.85 ms: 1.01x faster                                                   |
| regex_compile  | 134 ms                                                                 | 134 ms: 1.01x slower                                                    |
| regex_v8       | 25.8 ms                                                                | 26.3 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle               | 12.0 us                                                                | 11.6 us: 1.03x faster                                                   |
| unpickle             | 15.5 us                                                                | 15.0 us: 1.03x faster                                                   |
| tomli_loads          | 2.19 sec                                                               | 2.14 sec: 1.02x faster                                                  |
| pickle_dict          | 35.1 us                                                                | 34.4 us: 1.02x faster                                                   |
| xml_etree_iterparse  | 108 ms                                                                 | 107 ms: 1.01x faster                                                    |
| pickle_pure_python   | 303 us                                                                 | 299 us: 1.01x faster                                                    |
| unpickle_pure_python | 215 us                                                                 | 213 us: 1.01x faster                                                    |
| json_loads           | 27.5 us                                                                | 27.4 us: 1.00x faster                                                   |
| xml_etree_generate   | 86.3 ms                                                                | 86.7 ms: 1.00x slower                                                   |
| unpickle_list        | 5.16 us                                                                | 5.19 us: 1.01x slower                                                   |
| pickle_list          | 5.11 us                                                                | 5.21 us: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (3): xml_etree_parse, json_dumps, xml_etree_process

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 35.1 ms                                                                | 34.4 ms: 1.02x faster                                                   |
| mako            | 11.0 ms                                                                | 10.9 ms: 1.01x faster                                                   |
| genshi_xml      | 51.3 ms                                                                | 51.1 ms: 1.00x faster                                                   |
| genshi_text     | 23.1 ms                                                                | 23.2 ms: 1.01x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                            |

All benchmarks:
===============

| Benchmark                | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits                 | 215 ms                                                                 | 194 ms: 1.11x faster                                                    |
| gc_traversal             | 3.77 ms                                                                | 3.55 ms: 1.06x faster                                                   |
| scimark_sor              | 130 ms                                                                 | 124 ms: 1.05x faster                                                    |
| logging_silent           | 100 ns                                                                 | 96.3 ns: 1.04x faster                                                   |
| html5lib                 | 67.9 ms                                                                | 65.6 ms: 1.04x faster                                                   |
| pickle                   | 12.0 us                                                                | 11.6 us: 1.03x faster                                                   |
| scimark_fft              | 376 ms                                                                 | 365 ms: 1.03x faster                                                    |
| unpickle                 | 15.5 us                                                                | 15.0 us: 1.03x faster                                                   |
| nbody                    | 89.9 ms                                                                | 87.4 ms: 1.03x faster                                                   |
| hexiom                   | 6.29 ms                                                                | 6.15 ms: 1.02x faster                                                   |
| tomli_loads              | 2.19 sec                                                               | 2.14 sec: 1.02x faster                                                  |
| django_template          | 35.1 ms                                                                | 34.4 ms: 1.02x faster                                                   |
| pickle_dict              | 35.1 us                                                                | 34.4 us: 1.02x faster                                                   |
| scimark_sparse_mat_mult  | 5.27 ms                                                                | 5.17 ms: 1.02x faster                                                   |
| thrift                   | 830 us                                                                 | 816 us: 1.02x faster                                                    |
| xml_etree_iterparse      | 108 ms                                                                 | 107 ms: 1.01x faster                                                    |
| fannkuch                 | 388 ms                                                                 | 383 ms: 1.01x faster                                                    |
| regex_effbot             | 3.90 ms                                                                | 3.85 ms: 1.01x faster                                                   |
| scimark_monte_carlo      | 68.1 ms                                                                | 67.2 ms: 1.01x faster                                                   |
| pickle_pure_python       | 303 us                                                                 | 299 us: 1.01x faster                                                    |
| mako                     | 11.0 ms                                                                | 10.9 ms: 1.01x faster                                                   |
| meteor_contest           | 111 ms                                                                 | 110 ms: 1.01x faster                                                    |
| pycparser                | 1.21 sec                                                               | 1.20 sec: 1.01x faster                                                  |
| create_gc_cycles         | 1.77 ms                                                                | 1.75 ms: 1.01x faster                                                   |
| pprint_pformat           | 1.53 sec                                                               | 1.52 sec: 1.01x faster                                                  |
| unpickle_pure_python     | 215 us                                                                 | 213 us: 1.01x faster                                                    |
| mdp                      | 2.82 sec                                                               | 2.79 sec: 1.01x faster                                                  |
| telco                    | 8.55 ms                                                                | 8.49 ms: 1.01x faster                                                   |
| pprint_safe_repr         | 748 ms                                                                 | 742 ms: 1.01x faster                                                    |
| sqlglot_normalize        | 110 ms                                                                 | 109 ms: 1.01x faster                                                    |
| async_generators         | 444 ms                                                                 | 440 ms: 1.01x faster                                                    |
| 2to3                     | 269 ms                                                                 | 267 ms: 1.01x faster                                                    |
| asyncio_tcp              | 510 ms                                                                 | 506 ms: 1.01x faster                                                    |
| sqlglot_optimize         | 55.0 ms                                                                | 54.7 ms: 1.01x faster                                                   |
| genshi_xml               | 51.3 ms                                                                | 51.1 ms: 1.00x faster                                                   |
| docutils                 | 2.81 sec                                                               | 2.80 sec: 1.00x faster                                                  |
| asyncio_tcp_ssl          | 1.84 sec                                                               | 1.84 sec: 1.00x faster                                                  |
| json_loads               | 27.5 us                                                                | 27.4 us: 1.00x faster                                                   |
| pyflate                  | 465 ms                                                                 | 464 ms: 1.00x faster                                                    |
| deepcopy                 | 353 us                                                                 | 355 us: 1.00x slower                                                    |
| xml_etree_generate       | 86.3 ms                                                                | 86.7 ms: 1.00x slower                                                   |
| richards_super           | 52.9 ms                                                                | 53.2 ms: 1.00x slower                                                   |
| generators               | 29.7 ms                                                                | 29.8 ms: 1.00x slower                                                   |
| dulwich_log              | 65.7 ms                                                                | 66.0 ms: 1.00x slower                                                   |
| sqlglot_parse            | 1.29 ms                                                                | 1.29 ms: 1.01x slower                                                   |
| regex_compile            | 134 ms                                                                 | 134 ms: 1.01x slower                                                    |
| unpickle_list            | 5.16 us                                                                | 5.19 us: 1.01x slower                                                   |
| genshi_text              | 23.1 ms                                                                | 23.2 ms: 1.01x slower                                                   |
| crypto_pyaes             | 74.5 ms                                                                | 75.2 ms: 1.01x slower                                                   |
| chaos                    | 59.7 ms                                                                | 60.3 ms: 1.01x slower                                                   |
| float                    | 78.0 ms                                                                | 78.8 ms: 1.01x slower                                                   |
| deepcopy_memo            | 38.7 us                                                                | 39.1 us: 1.01x slower                                                   |
| richards                 | 46.5 ms                                                                | 47.0 ms: 1.01x slower                                                   |
| typing_runtime_protocols | 161 us                                                                 | 163 us: 1.01x slower                                                    |
| scimark_lu               | 116 ms                                                                 | 118 ms: 1.01x slower                                                    |
| nqueens                  | 80.4 ms                                                                | 81.6 ms: 1.01x slower                                                   |
| deepcopy_reduce          | 3.15 us                                                                | 3.21 us: 1.02x slower                                                   |
| pickle_list              | 5.11 us                                                                | 5.21 us: 1.02x slower                                                   |
| regex_v8                 | 25.8 ms                                                                | 26.3 ms: 1.02x slower                                                   |
| raytrace                 | 260 ms                                                                 | 267 ms: 1.03x slower                                                    |
| spectral_norm            | 112 ms                                                                 | 116 ms: 1.04x slower                                                    |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (40): async_tree_none_tg, async_tree_io, async_tree_memoization_tg, async_tree_io_tg, deltablue, xml_etree_parse, async_tree_none, pylint, sympy_str, sympy_sum, logging_format, bench_thread_pool, json, asyncio_websockets, sympy_expand, chameleon, pathlib, dask, sympy_integrate, go, json_dumps, python_startup, coroutines, python_startup_no_site, tornado_http, sqlglot_transpile, xml_etree_process, bench_mp_pool, regex_dna, gunicorn, comprehensions, logging_simple, sqlite_synth, async_tree_memoization, coverage, djangocms, aiohttp, mypy2, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

# HPT report

- Reliability score: 98.82% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x