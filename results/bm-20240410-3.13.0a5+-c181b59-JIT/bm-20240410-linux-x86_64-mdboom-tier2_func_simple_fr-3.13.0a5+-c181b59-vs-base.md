# Results vs. base

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.00x faster
- HPT reliability: 99.88%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 278 ms                                                                 | 279 ms: 1.00x slower                                                   |
| chameleon      | 7.12 ms                                                                | 7.06 ms: 1.01x faster                                                  |
| html5lib       | 66.7 ms                                                                | 68.0 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.3 ms                                                                | 78.0 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.73 ms                                                                | 3.59 ms: 1.04x faster                                                  |
| regex_dna      | 225 ms                                                                 | 221 ms: 1.02x faster                                                   |
| regex_compile  | 143 ms                                                                 | 144 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|--------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle           | 17.4 us                                                                | 14.9 us: 1.17x faster                                                  |
| unpickle_list      | 5.31 us                                                                | 5.15 us: 1.03x faster                                                  |
| json_dumps         | 10.4 ms                                                                | 10.4 ms: 1.01x faster                                                  |
| xml_etree_generate | 88.0 ms                                                                | 88.7 ms: 1.01x slower                                                  |
| tomli_loads        | 2.05 sec                                                               | 2.07 sec: 1.01x slower                                                 |
| pickle_list        | 4.96 us                                                                | 5.01 us: 1.01x slower                                                  |
| xml_etree_process  | 60.4 ms                                                                | 61.5 ms: 1.02x slower                                                  |
| pickle             | 11.7 us                                                                | 11.9 us: 1.02x slower                                                  |
| pickle_dict        | 34.2 us                                                                | 35.1 us: 1.03x slower                                                  |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (5): xml_etree_parse, pickle_pure_python, xml_etree_iterparse, json_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 9.52 ms                                                                | 9.50 ms: 1.00x faster                                                  |
| python_startup         | 11.1 ms                                                                | 11.0 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 24.7 ms                                                                | 24.2 ms: 1.02x faster                                                  |
| genshi_xml     | 54.5 ms                                                                | 53.5 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|--------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle                 | 17.4 us                                                                | 14.9 us: 1.17x faster                                                  |
| scimark_sor              | 141 ms                                                                 | 134 ms: 1.05x faster                                                   |
| regex_effbot             | 3.73 ms                                                                | 3.59 ms: 1.04x faster                                                  |
| unpickle_list            | 5.31 us                                                                | 5.15 us: 1.03x faster                                                  |
| deepcopy_memo            | 39.5 us                                                                | 38.4 us: 1.03x faster                                                  |
| pyflate                  | 476 ms                                                                 | 464 ms: 1.03x faster                                                   |
| logging_simple           | 5.94 us                                                                | 5.80 us: 1.02x faster                                                  |
| scimark_sparse_mat_mult  | 5.02 ms                                                                | 4.91 ms: 1.02x faster                                                  |
| gc_traversal             | 4.04 ms                                                                | 3.96 ms: 1.02x faster                                                  |
| regex_dna                | 225 ms                                                                 | 221 ms: 1.02x faster                                                   |
| genshi_text              | 24.7 ms                                                                | 24.2 ms: 1.02x faster                                                  |
| genshi_xml               | 54.5 ms                                                                | 53.5 ms: 1.02x faster                                                  |
| logging_format           | 6.49 us                                                                | 6.40 us: 1.01x faster                                                  |
| deepcopy_reduce          | 3.26 us                                                                | 3.21 us: 1.01x faster                                                  |
| typing_runtime_protocols | 115 us                                                                 | 113 us: 1.01x faster                                                   |
| scimark_fft              | 345 ms                                                                 | 342 ms: 1.01x faster                                                   |
| deepcopy                 | 366 us                                                                 | 363 us: 1.01x faster                                                   |
| thrift                   | 825 us                                                                 | 817 us: 1.01x faster                                                   |
| comprehensions           | 18.0 us                                                                | 17.9 us: 1.01x faster                                                  |
| json_dumps               | 10.4 ms                                                                | 10.4 ms: 1.01x faster                                                  |
| chameleon                | 7.12 ms                                                                | 7.06 ms: 1.01x faster                                                  |
| python_startup_no_site   | 9.52 ms                                                                | 9.50 ms: 1.00x faster                                                  |
| asyncio_tcp_ssl          | 1.86 sec                                                               | 1.86 sec: 1.00x faster                                                 |
| python_startup           | 11.1 ms                                                                | 11.0 ms: 1.00x faster                                                  |
| asyncio_tcp              | 513 ms                                                                 | 512 ms: 1.00x faster                                                   |
| pylint                   | 295 ms                                                                 | 296 ms: 1.00x slower                                                   |
| bench_thread_pool        | 855 us                                                                 | 858 us: 1.00x slower                                                   |
| 2to3                     | 278 ms                                                                 | 279 ms: 1.00x slower                                                   |
| go                       | 154 ms                                                                 | 155 ms: 1.00x slower                                                   |
| chaos                    | 62.3 ms                                                                | 62.6 ms: 1.00x slower                                                  |
| sympy_str                | 296 ms                                                                 | 297 ms: 1.01x slower                                                   |
| fannkuch                 | 398 ms                                                                 | 400 ms: 1.01x slower                                                   |
| sympy_sum                | 167 ms                                                                 | 168 ms: 1.01x slower                                                   |
| sympy_integrate          | 22.0 ms                                                                | 22.1 ms: 1.01x slower                                                  |
| sympy_expand             | 494 ms                                                                 | 497 ms: 1.01x slower                                                   |
| richards                 | 43.6 ms                                                                | 44.0 ms: 1.01x slower                                                  |
| dulwich_log              | 70.1 ms                                                                | 70.6 ms: 1.01x slower                                                  |
| hexiom                   | 6.99 ms                                                                | 7.04 ms: 1.01x slower                                                  |
| scimark_lu               | 133 ms                                                                 | 134 ms: 1.01x slower                                                   |
| create_gc_cycles         | 1.75 ms                                                                | 1.76 ms: 1.01x slower                                                  |
| xml_etree_generate       | 88.0 ms                                                                | 88.7 ms: 1.01x slower                                                  |
| float                    | 77.3 ms                                                                | 78.0 ms: 1.01x slower                                                  |
| async_generators         | 458 ms                                                                 | 462 ms: 1.01x slower                                                   |
| tomli_loads              | 2.05 sec                                                               | 2.07 sec: 1.01x slower                                                 |
| generators               | 30.0 ms                                                                | 30.2 ms: 1.01x slower                                                  |
| pickle_list              | 4.96 us                                                                | 5.01 us: 1.01x slower                                                  |
| regex_compile            | 143 ms                                                                 | 144 ms: 1.01x slower                                                   |
| richards_super           | 49.5 ms                                                                | 50.1 ms: 1.01x slower                                                  |
| sqlglot_optimize         | 57.5 ms                                                                | 58.2 ms: 1.01x slower                                                  |
| nqueens                  | 89.8 ms                                                                | 90.9 ms: 1.01x slower                                                  |
| coverage                 | 97.8 ms                                                                | 99.0 ms: 1.01x slower                                                  |
| telco                    | 8.66 ms                                                                | 8.79 ms: 1.02x slower                                                  |
| sqlglot_normalize        | 113 ms                                                                 | 115 ms: 1.02x slower                                                   |
| raytrace                 | 273 ms                                                                 | 278 ms: 1.02x slower                                                   |
| mdp                      | 2.77 sec                                                               | 2.82 sec: 1.02x slower                                                 |
| logging_silent           | 100 ns                                                                 | 102 ns: 1.02x slower                                                   |
| xml_etree_process        | 60.4 ms                                                                | 61.5 ms: 1.02x slower                                                  |
| html5lib                 | 66.7 ms                                                                | 68.0 ms: 1.02x slower                                                  |
| pickle                   | 11.7 us                                                                | 11.9 us: 1.02x slower                                                  |
| pickle_dict              | 34.2 us                                                                | 35.1 us: 1.03x slower                                                  |
| pprint_pformat           | 1.52 sec                                                               | 1.56 sec: 1.03x slower                                                 |
| coroutines               | 22.2 ms                                                                | 22.8 ms: 1.03x slower                                                  |
| pprint_safe_repr         | 743 ms                                                                 | 775 ms: 1.04x slower                                                   |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (36): xml_etree_parse, async_tree_io, async_tree_memoization, deltablue, sqlite_synth, scimark_monte_carlo, dask, sqlglot_transpile, sqlglot_parse, bench_mp_pool, pickle_pure_python, nbody, gunicorn, docutils, meteor_contest, xml_etree_iterparse, async_tree_none, tornado_http, json, pidigits, json_loads, asyncio_websockets, async_tree_cpu_io_mixed, async_tree_memoization_tg, regex_v8, mako, spectral_norm, unpickle_pure_python, async_tree_cpu_io_mixed_tg, pycparser, pathlib, mypy2, crypto_pyaes, aiohttp, async_tree_none_tg, async_tree_io_tg

# HPT report

- Reliability score: 99.88% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x