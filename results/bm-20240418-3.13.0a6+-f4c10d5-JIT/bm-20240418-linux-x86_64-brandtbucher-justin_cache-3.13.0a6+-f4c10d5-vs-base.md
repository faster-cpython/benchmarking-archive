# Results vs. base

- fork: brandtbucher
- ref: justin_cache
- machine: linux-x86_64
- commit hash: f4c10d5
- commit date: 2024-04-18
- overall geometric mean: 1.00x slower
- HPT reliability: 99.71%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 278 ms: 1.00x slower                                                 |
| chameleon      | 6.94 ms                                                                | 7.08 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_io, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 90.9 ms                                                                | 87.3 ms: 1.04x faster                                                |
| pidigits       | 211 ms                                                                 | 210 ms: 1.00x faster                                                 |
| float          | 77.0 ms                                                                | 77.7 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 25.9 ms                                                                | 25.0 ms: 1.03x faster                                                |
| regex_dna      | 227 ms                                                                 | 221 ms: 1.03x faster                                                 |
| regex_compile  | 143 ms                                                                 | 144 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle           | 16.8 us                                                                | 15.7 us: 1.06x faster                                                |
| unpickle_list      | 5.33 us                                                                | 5.27 us: 1.01x faster                                                |
| xml_etree_generate | 87.8 ms                                                                | 88.1 ms: 1.00x slower                                                |
| pickle_list        | 5.06 us                                                                | 5.33 us: 1.05x slower                                                |
| pickle_dict        | 33.9 us                                                                | 36.0 us: 1.06x slower                                                |
| Geometric mean     | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (9): json_dumps, xml_etree_process, tomli_loads, unpickle_pure_python, pickle, xml_etree_iterparse, json_loads, pickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                |
| python_startup_no_site | 7.59 ms                                                                | 7.69 ms: 1.01x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 36.5 ms                                                                | 36.2 ms: 1.01x faster                                                |
| mako            | 10.7 ms                                                                | 11.5 ms: 1.08x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                         |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark              | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle               | 16.8 us                                                                | 15.7 us: 1.06x faster                                                |
| mdp                    | 2.81 sec                                                               | 2.64 sec: 1.06x faster                                               |
| nbody                  | 90.9 ms                                                                | 87.3 ms: 1.04x faster                                                |
| pycparser              | 1.21 sec                                                               | 1.17 sec: 1.04x faster                                               |
| go                     | 153 ms                                                                 | 148 ms: 1.04x faster                                                 |
| scimark_monte_carlo    | 70.2 ms                                                                | 67.9 ms: 1.03x faster                                                |
| regex_v8               | 25.9 ms                                                                | 25.0 ms: 1.03x faster                                                |
| regex_dna              | 227 ms                                                                 | 221 ms: 1.03x faster                                                 |
| pprint_pformat         | 1.58 sec                                                               | 1.54 sec: 1.03x faster                                               |
| fannkuch               | 399 ms                                                                 | 389 ms: 1.02x faster                                                 |
| telco                  | 8.72 ms                                                                | 8.56 ms: 1.02x faster                                                |
| unpickle_list          | 5.33 us                                                                | 5.27 us: 1.01x faster                                                |
| deepcopy_memo          | 38.6 us                                                                | 38.2 us: 1.01x faster                                                |
| django_template        | 36.5 ms                                                                | 36.2 ms: 1.01x faster                                                |
| logging_simple         | 5.80 us                                                                | 5.75 us: 1.01x faster                                                |
| deepcopy               | 359 us                                                                 | 356 us: 1.01x faster                                                 |
| sqlite_synth           | 2.90 us                                                                | 2.88 us: 1.01x faster                                                |
| crypto_pyaes           | 74.4 ms                                                                | 73.9 ms: 1.01x faster                                                |
| coverage               | 98.7 ms                                                                | 98.2 ms: 1.01x faster                                                |
| scimark_fft            | 342 ms                                                                 | 341 ms: 1.00x faster                                                 |
| pidigits               | 211 ms                                                                 | 210 ms: 1.00x faster                                                 |
| asyncio_tcp_ssl        | 1.85 sec                                                               | 1.86 sec: 1.00x slower                                               |
| asyncio_tcp            | 510 ms                                                                 | 512 ms: 1.00x slower                                                 |
| xml_etree_generate     | 87.8 ms                                                                | 88.1 ms: 1.00x slower                                                |
| 2to3                   | 277 ms                                                                 | 278 ms: 1.00x slower                                                 |
| sympy_integrate        | 22.0 ms                                                                | 22.1 ms: 1.00x slower                                                |
| bench_thread_pool      | 860 us                                                                 | 863 us: 1.00x slower                                                 |
| sqlglot_transpile      | 1.64 ms                                                                | 1.65 ms: 1.01x slower                                                |
| sympy_str              | 297 ms                                                                 | 299 ms: 1.01x slower                                                 |
| dulwich_log            | 69.3 ms                                                                | 69.9 ms: 1.01x slower                                                |
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                |
| regex_compile          | 143 ms                                                                 | 144 ms: 1.01x slower                                                 |
| float                  | 77.0 ms                                                                | 77.7 ms: 1.01x slower                                                |
| pprint_safe_repr       | 743 ms                                                                 | 751 ms: 1.01x slower                                                 |
| raytrace               | 272 ms                                                                 | 275 ms: 1.01x slower                                                 |
| pyflate                | 474 ms                                                                 | 479 ms: 1.01x slower                                                 |
| pathlib                | 17.7 ms                                                                | 17.8 ms: 1.01x slower                                                |
| sqlglot_parse          | 1.32 ms                                                                | 1.33 ms: 1.01x slower                                                |
| python_startup_no_site | 7.59 ms                                                                | 7.69 ms: 1.01x slower                                                |
| generators             | 30.1 ms                                                                | 30.5 ms: 1.01x slower                                                |
| sympy_expand           | 494 ms                                                                 | 501 ms: 1.01x slower                                                 |
| logging_silent         | 101 ns                                                                 | 103 ns: 1.01x slower                                                 |
| hexiom                 | 6.99 ms                                                                | 7.09 ms: 1.01x slower                                                |
| spectral_norm          | 114 ms                                                                 | 116 ms: 1.02x slower                                                 |
| sympy_sum              | 167 ms                                                                 | 170 ms: 1.02x slower                                                 |
| gc_traversal           | 3.79 ms                                                                | 3.85 ms: 1.02x slower                                                |
| meteor_contest         | 110 ms                                                                 | 113 ms: 1.02x slower                                                 |
| comprehensions         | 18.0 us                                                                | 18.3 us: 1.02x slower                                                |
| coroutines             | 22.7 ms                                                                | 23.1 ms: 1.02x slower                                                |
| chameleon              | 6.94 ms                                                                | 7.08 ms: 1.02x slower                                                |
| scimark_lu             | 131 ms                                                                 | 134 ms: 1.03x slower                                                 |
| djangocms              | 31.2 us                                                                | 32.2 us: 1.03x slower                                                |
| nqueens                | 89.3 ms                                                                | 93.0 ms: 1.04x slower                                                |
| pickle_list            | 5.06 us                                                                | 5.33 us: 1.05x slower                                                |
| pickle_dict            | 33.9 us                                                                | 36.0 us: 1.06x slower                                                |
| mako                   | 10.7 ms                                                                | 11.5 ms: 1.08x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (45): json, sqlglot_optimize, logging_format, json_dumps, richards_super, sqlglot_normalize, async_generators, async_tree_memoization, xml_etree_process, tomli_loads, typing_runtime_protocols, scimark_sparse_mat_mult, deepcopy_reduce, create_gc_cycles, unpickle_pure_python, dask, aiohttp, bench_mp_pool, pickle, regex_effbot, pylint, async_tree_cpu_io_mixed_tg, asyncio_websockets, html5lib, xml_etree_iterparse, async_tree_memoization_tg, mypy2, docutils, async_tree_none_tg, json_loads, scimark_sor, tornado_http, thrift, gunicorn, pickle_pure_python, xml_etree_parse, chaos, async_tree_cpu_io_mixed, genshi_xml, genshi_text, async_tree_io_tg, richards, deltablue, async_tree_io, async_tree_none

# HPT report

- Reliability score: 99.71% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.03x