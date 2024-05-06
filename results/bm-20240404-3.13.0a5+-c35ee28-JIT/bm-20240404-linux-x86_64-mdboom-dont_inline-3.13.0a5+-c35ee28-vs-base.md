# Results vs. base

- fork: mdboom
- ref: dont_inline
- machine: linux-x86_64
- commit hash: c35ee28
- commit date: 2024-04-04
- overall geometric mean: 1.01x slower
- HPT reliability: 61.66%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| docutils       | 2.90 sec                                                               | 2.92 sec: 1.01x slower                                        |
| html5lib       | 65.5 ms                                                                | 67.7 ms: 1.03x slower                                         |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                  |

Benchmark hidden because not significant (3): 2to3, chameleon, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_none, async_tree_io, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| float          | 76.2 ms                                                                | 76.9 ms: 1.01x slower                                         |
| pidigits       | 202 ms                                                                 | 207 ms: 1.02x slower                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                  |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_compile  | 146 ms                                                                 | 147 ms: 1.01x slower                                          |
| regex_v8       | 25.0 ms                                                                | 25.8 ms: 1.04x slower                                         |
| regex_effbot   | 3.60 ms                                                                | 3.78 ms: 1.05x slower                                         |
| regex_dna      | 220 ms                                                                 | 233 ms: 1.06x slower                                          |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| pickle               | 12.0 us                                                                | 11.7 us: 1.03x faster                                         |
| json_dumps           | 10.7 ms                                                                | 10.4 ms: 1.02x faster                                         |
| pickle_list          | 5.02 us                                                                | 4.96 us: 1.01x faster                                         |
| json_loads           | 28.8 us                                                                | 28.6 us: 1.01x faster                                         |
| unpickle_pure_python | 236 us                                                                 | 239 us: 1.01x slower                                          |
| xml_etree_parse      | 159 ms                                                                 | 162 ms: 1.02x slower                                          |
| unpickle_list        | 5.18 us                                                                | 5.29 us: 1.02x slower                                         |
| unpickle             | 14.8 us                                                                | 16.2 us: 1.10x slower                                         |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                  |

Benchmark hidden because not significant (6): xml_etree_generate, pickle_dict, xml_etree_process, tomli_loads, xml_etree_iterparse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup_no_site | 9.49 ms                                                                | 9.52 ms: 1.00x slower                                         |
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.00x slower                                         |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| mako           | 10.9 ms                                                                | 10.8 ms: 1.01x faster                                         |
| genshi_text    | 24.6 ms                                                                | 24.8 ms: 1.01x slower                                         |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                  |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|--------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| scimark_sparse_mat_mult  | 5.02 ms                                                                | 4.84 ms: 1.04x faster                                         |
| pickle                   | 12.0 us                                                                | 11.7 us: 1.03x faster                                         |
| json_dumps               | 10.7 ms                                                                | 10.4 ms: 1.02x faster                                         |
| deepcopy                 | 364 us                                                                 | 358 us: 1.02x faster                                          |
| json                     | 5.44 ms                                                                | 5.36 ms: 1.01x faster                                         |
| mako                     | 10.9 ms                                                                | 10.8 ms: 1.01x faster                                         |
| pickle_list              | 5.02 us                                                                | 4.96 us: 1.01x faster                                         |
| sqlglot_normalize        | 114 ms                                                                 | 113 ms: 1.01x faster                                          |
| asyncio_tcp              | 520 ms                                                                 | 515 ms: 1.01x faster                                          |
| pathlib                  | 19.1 ms                                                                | 18.9 ms: 1.01x faster                                         |
| scimark_fft              | 346 ms                                                                 | 343 ms: 1.01x faster                                          |
| json_loads               | 28.8 us                                                                | 28.6 us: 1.01x faster                                         |
| scimark_monte_carlo      | 69.3 ms                                                                | 68.8 ms: 1.01x faster                                         |
| sympy_integrate          | 22.0 ms                                                                | 21.9 ms: 1.01x faster                                         |
| create_gc_cycles         | 1.76 ms                                                                | 1.75 ms: 1.00x faster                                         |
| sqlglot_optimize         | 58.0 ms                                                                | 57.7 ms: 1.00x faster                                         |
| generators               | 29.7 ms                                                                | 29.5 ms: 1.00x faster                                         |
| sqlglot_transpile        | 1.64 ms                                                                | 1.63 ms: 1.00x faster                                         |
| dulwich_log              | 71.2 ms                                                                | 70.9 ms: 1.00x faster                                         |
| asyncio_tcp_ssl          | 1.86 sec                                                               | 1.86 sec: 1.00x faster                                        |
| python_startup_no_site   | 9.49 ms                                                                | 9.52 ms: 1.00x slower                                         |
| python_startup           | 11.0 ms                                                                | 11.1 ms: 1.00x slower                                         |
| asyncio_websockets       | 564 ms                                                                 | 566 ms: 1.00x slower                                          |
| spectral_norm            | 115 ms                                                                 | 115 ms: 1.01x slower                                          |
| deepcopy_memo            | 38.5 us                                                                | 38.8 us: 1.01x slower                                         |
| docutils                 | 2.90 sec                                                               | 2.92 sec: 1.01x slower                                        |
| deltablue                | 3.42 ms                                                                | 3.45 ms: 1.01x slower                                         |
| regex_compile            | 146 ms                                                                 | 147 ms: 1.01x slower                                          |
| richards                 | 45.9 ms                                                                | 46.3 ms: 1.01x slower                                         |
| sqlite_synth             | 2.85 us                                                                | 2.88 us: 1.01x slower                                         |
| float                    | 76.2 ms                                                                | 76.9 ms: 1.01x slower                                         |
| go                       | 153 ms                                                                 | 154 ms: 1.01x slower                                          |
| meteor_contest           | 111 ms                                                                 | 112 ms: 1.01x slower                                          |
| scimark_lu               | 132 ms                                                                 | 133 ms: 1.01x slower                                          |
| genshi_text              | 24.6 ms                                                                | 24.8 ms: 1.01x slower                                         |
| richards_super           | 52.2 ms                                                                | 52.7 ms: 1.01x slower                                         |
| unpickle_pure_python     | 236 us                                                                 | 239 us: 1.01x slower                                          |
| comprehensions           | 17.9 us                                                                | 18.1 us: 1.01x slower                                         |
| deepcopy_reduce          | 3.23 us                                                                | 3.27 us: 1.01x slower                                         |
| xml_etree_parse          | 159 ms                                                                 | 162 ms: 1.02x slower                                          |
| pyflate                  | 469 ms                                                                 | 476 ms: 1.02x slower                                          |
| coverage                 | 98.1 ms                                                                | 100 ms: 1.02x slower                                          |
| pprint_safe_repr         | 733 ms                                                                 | 748 ms: 1.02x slower                                          |
| unpickle_list            | 5.18 us                                                                | 5.29 us: 1.02x slower                                         |
| pidigits                 | 202 ms                                                                 | 207 ms: 1.02x slower                                          |
| coroutines               | 22.2 ms                                                                | 22.7 ms: 1.02x slower                                         |
| typing_runtime_protocols | 111 us                                                                 | 114 us: 1.03x slower                                          |
| html5lib                 | 65.5 ms                                                                | 67.7 ms: 1.03x slower                                         |
| regex_v8                 | 25.0 ms                                                                | 25.8 ms: 1.04x slower                                         |
| pycparser                | 1.16 sec                                                               | 1.21 sec: 1.05x slower                                        |
| logging_silent           | 97.9 ns                                                                | 103 ns: 1.05x slower                                          |
| regex_effbot             | 3.60 ms                                                                | 3.78 ms: 1.05x slower                                         |
| regex_dna                | 220 ms                                                                 | 233 ms: 1.06x slower                                          |
| mdp                      | 2.63 sec                                                               | 2.83 sec: 1.07x slower                                        |
| unpickle                 | 14.8 us                                                                | 16.2 us: 1.10x slower                                         |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                  |

Benchmark hidden because not significant (44): async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_cpu_io_mixed, nbody, dask, chaos, thrift, raytrace, async_tree_memoization_tg, sympy_expand, sympy_sum, telco, async_tree_none, xml_etree_generate, pickle_dict, pylint, xml_etree_process, tomli_loads, tornado_http, aiohttp, bench_thread_pool, async_tree_io, sqlglot_parse, 2to3, xml_etree_iterparse, chameleon, sympy_str, gc_traversal, pprint_pformat, logging_simple, hexiom, logging_format, mypy2, scimark_sor, pickle_pure_python, async_generators, gunicorn, bench_mp_pool, genshi_xml, fannkuch, crypto_pyaes, nqueens, async_tree_memoization

# HPT report

- Reliability score: 61.66% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x