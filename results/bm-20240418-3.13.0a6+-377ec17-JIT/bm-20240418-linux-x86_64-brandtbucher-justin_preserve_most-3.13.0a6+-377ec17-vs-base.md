# Results vs. base

- fork: brandtbucher
- ref: justin_preserve_most
- machine: linux-x86_64
- commit hash: 377ec17
- commit date: 2024-04-18
- overall geometric mean: 1.00x faster
- HPT reliability: 99.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 276 ms: 1.01x faster                                                         |
| docutils       | 2.92 sec                                                               | 2.90 sec: 1.01x faster                                                       |
| tornado_http   | 96.4 ms                                                                | 96.0 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                 |

Benchmark hidden because not significant (2): chameleon, html5lib

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none, async_tree_io_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 211 ms                                                                 | 190 ms: 1.11x faster                                                         |
| float          | 77.0 ms                                                                | 76.6 ms: 1.00x faster                                                        |
| nbody          | 90.9 ms                                                                | 95.1 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 25.9 ms                                                                | 25.3 ms: 1.02x faster                                                        |
| regex_compile  | 143 ms                                                                 | 142 ms: 1.01x faster                                                         |
| regex_dna      | 227 ms                                                                 | 228 ms: 1.01x slower                                                         |
| regex_effbot   | 3.67 ms                                                                | 3.78 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle             | 16.8 us                                                                | 15.2 us: 1.11x faster                                                        |
| unpickle_list        | 5.33 us                                                                | 5.00 us: 1.07x faster                                                        |
| pickle               | 12.0 us                                                                | 11.7 us: 1.03x faster                                                        |
| unpickle_pure_python | 236 us                                                                 | 231 us: 1.02x faster                                                         |
| xml_etree_iterparse  | 109 ms                                                                 | 107 ms: 1.02x faster                                                         |
| tomli_loads          | 2.02 sec                                                               | 1.99 sec: 1.02x faster                                                       |
| xml_etree_process    | 60.5 ms                                                                | 60.0 ms: 1.01x faster                                                        |
| xml_etree_generate   | 87.8 ms                                                                | 87.2 ms: 1.01x faster                                                        |
| json_loads           | 27.7 us                                                                | 27.8 us: 1.00x slower                                                        |
| pickle_list          | 5.06 us                                                                | 5.15 us: 1.02x slower                                                        |
| pickle_dict          | 33.9 us                                                                | 35.7 us: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                 |

Benchmark hidden because not significant (3): json_dumps, pickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 10.9 ms: 1.01x faster                                                        |
| python_startup_no_site | 7.59 ms                                                                | 7.55 ms: 1.01x faster                                                        |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 36.5 ms                                                                | 35.9 ms: 1.02x faster                                                        |
| mako            | 10.7 ms                                                                | 10.6 ms: 1.01x faster                                                        |
| genshi_xml      | 54.4 ms                                                                | 53.9 ms: 1.01x faster                                                        |
| genshi_text     | 24.2 ms                                                                | 24.0 ms: 1.01x faster                                                        |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20240416-linux-x86_64-python-241ed5f2cdd525de0e13-3.13.0a6+-241ed5f | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|--------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits                 | 211 ms                                                                 | 190 ms: 1.11x faster                                                         |
| unpickle                 | 16.8 us                                                                | 15.2 us: 1.11x faster                                                        |
| mdp                      | 2.81 sec                                                               | 2.62 sec: 1.07x faster                                                       |
| unpickle_list            | 5.33 us                                                                | 5.00 us: 1.07x faster                                                        |
| scimark_monte_carlo      | 70.2 ms                                                                | 67.8 ms: 1.03x faster                                                        |
| comprehensions           | 18.0 us                                                                | 17.4 us: 1.03x faster                                                        |
| pickle                   | 12.0 us                                                                | 11.7 us: 1.03x faster                                                        |
| richards                 | 43.2 ms                                                                | 42.1 ms: 1.03x faster                                                        |
| pyflate                  | 474 ms                                                                 | 463 ms: 1.02x faster                                                         |
| regex_v8                 | 25.9 ms                                                                | 25.3 ms: 1.02x faster                                                        |
| unpickle_pure_python     | 236 us                                                                 | 231 us: 1.02x faster                                                         |
| hexiom                   | 6.99 ms                                                                | 6.86 ms: 1.02x faster                                                        |
| fannkuch                 | 399 ms                                                                 | 392 ms: 1.02x faster                                                         |
| django_template          | 36.5 ms                                                                | 35.9 ms: 1.02x faster                                                        |
| xml_etree_iterparse      | 109 ms                                                                 | 107 ms: 1.02x faster                                                         |
| tomli_loads              | 2.02 sec                                                               | 1.99 sec: 1.02x faster                                                       |
| richards_super           | 49.2 ms                                                                | 48.4 ms: 1.02x faster                                                        |
| deepcopy_reduce          | 3.19 us                                                                | 3.14 us: 1.01x faster                                                        |
| mako                     | 10.7 ms                                                                | 10.6 ms: 1.01x faster                                                        |
| raytrace                 | 272 ms                                                                 | 269 ms: 1.01x faster                                                         |
| genshi_xml               | 54.4 ms                                                                | 53.9 ms: 1.01x faster                                                        |
| telco                    | 8.72 ms                                                                | 8.64 ms: 1.01x faster                                                        |
| python_startup           | 11.0 ms                                                                | 10.9 ms: 1.01x faster                                                        |
| chaos                    | 62.9 ms                                                                | 62.3 ms: 1.01x faster                                                        |
| genshi_text              | 24.2 ms                                                                | 24.0 ms: 1.01x faster                                                        |
| sqlglot_optimize         | 58.1 ms                                                                | 57.6 ms: 1.01x faster                                                        |
| xml_etree_process        | 60.5 ms                                                                | 60.0 ms: 1.01x faster                                                        |
| deepcopy                 | 359 us                                                                 | 356 us: 1.01x faster                                                         |
| sqlglot_transpile        | 1.64 ms                                                                | 1.63 ms: 1.01x faster                                                        |
| xml_etree_generate       | 87.8 ms                                                                | 87.2 ms: 1.01x faster                                                        |
| docutils                 | 2.92 sec                                                               | 2.90 sec: 1.01x faster                                                       |
| 2to3                     | 277 ms                                                                 | 276 ms: 1.01x faster                                                         |
| regex_compile            | 143 ms                                                                 | 142 ms: 1.01x faster                                                         |
| bench_thread_pool        | 860 us                                                                 | 855 us: 1.01x faster                                                         |
| python_startup_no_site   | 7.59 ms                                                                | 7.55 ms: 1.01x faster                                                        |
| float                    | 77.0 ms                                                                | 76.6 ms: 1.00x faster                                                        |
| sympy_integrate          | 22.0 ms                                                                | 21.9 ms: 1.00x faster                                                        |
| tornado_http             | 96.4 ms                                                                | 96.0 ms: 1.00x faster                                                        |
| create_gc_cycles         | 1.77 ms                                                                | 1.76 ms: 1.00x faster                                                        |
| json_loads               | 27.7 us                                                                | 27.8 us: 1.00x slower                                                        |
| sqlite_synth             | 2.90 us                                                                | 2.91 us: 1.00x slower                                                        |
| scimark_sor              | 132 ms                                                                 | 133 ms: 1.01x slower                                                         |
| regex_dna                | 227 ms                                                                 | 228 ms: 1.01x slower                                                         |
| coroutines               | 22.7 ms                                                                | 22.8 ms: 1.01x slower                                                        |
| sympy_expand             | 494 ms                                                                 | 498 ms: 1.01x slower                                                         |
| thrift                   | 819 us                                                                 | 826 us: 1.01x slower                                                         |
| meteor_contest           | 110 ms                                                                 | 112 ms: 1.01x slower                                                         |
| pathlib                  | 17.7 ms                                                                | 17.9 ms: 1.01x slower                                                        |
| typing_runtime_protocols | 112 us                                                                 | 114 us: 1.02x slower                                                         |
| pickle_list              | 5.06 us                                                                | 5.15 us: 1.02x slower                                                        |
| gc_traversal             | 3.79 ms                                                                | 3.89 ms: 1.03x slower                                                        |
| regex_effbot             | 3.67 ms                                                                | 3.78 ms: 1.03x slower                                                        |
| scimark_fft              | 342 ms                                                                 | 353 ms: 1.03x slower                                                         |
| djangocms                | 31.2 us                                                                | 32.4 us: 1.04x slower                                                        |
| spectral_norm            | 114 ms                                                                 | 119 ms: 1.04x slower                                                         |
| nbody                    | 90.9 ms                                                                | 95.1 ms: 1.05x slower                                                        |
| pickle_dict              | 33.9 us                                                                | 35.7 us: 1.05x slower                                                        |
| scimark_sparse_mat_mult  | 4.83 ms                                                                | 5.19 ms: 1.07x slower                                                        |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                                 |

Benchmark hidden because not significant (43): pprint_pformat, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, deepcopy_memo, async_tree_memoization_tg, aiohttp, deltablue, coverage, crypto_pyaes, json_dumps, pycparser, chameleon, bench_mp_pool, gunicorn, generators, pylint, asyncio_tcp_ssl, sympy_str, dulwich_log, logging_format, asyncio_websockets, asyncio_tcp, html5lib, async_tree_none, pickle_pure_python, mypy2, async_tree_io_tg, async_tree_io, go, scimark_lu, logging_simple, sqlglot_normalize, async_generators, logging_silent, sympy_sum, dask, nqueens, sqlglot_parse, xml_etree_parse, json, pprint_safe_repr

# HPT report

- Reliability score: 99.82% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x