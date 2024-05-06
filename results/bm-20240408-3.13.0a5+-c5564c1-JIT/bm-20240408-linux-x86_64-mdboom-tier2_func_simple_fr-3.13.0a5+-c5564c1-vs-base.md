# Results vs. base

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.00x slower
- HPT reliability: 99.75%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 2.92 sec                                                               | 2.94 sec: 1.00x slower                                                 |
| html5lib       | 66.7 ms                                                                | 68.5 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (3): 2to3, chameleon, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_none, async_tree_none_tg, async_tree_io_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.3 ms                                                                | 78.4 ms: 1.01x slower                                                  |
| pidigits       | 189 ms                                                                 | 211 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 143 ms                                                                 | 145 ms: 1.02x slower                                                   |
| regex_effbot   | 3.73 ms                                                                | 3.80 ms: 1.02x slower                                                  |
| regex_dna      | 225 ms                                                                 | 230 ms: 1.02x slower                                                   |
| regex_v8       | 25.0 ms                                                                | 26.0 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle             | 17.4 us                                                                | 15.0 us: 1.16x faster                                                  |
| json_loads           | 28.4 us                                                                | 28.2 us: 1.01x faster                                                  |
| json_dumps           | 10.4 ms                                                                | 10.4 ms: 1.00x faster                                                  |
| unpickle_pure_python | 242 us                                                                 | 240 us: 1.00x faster                                                   |
| xml_etree_generate   | 88.0 ms                                                                | 87.7 ms: 1.00x faster                                                  |
| tomli_loads          | 2.05 sec                                                               | 2.07 sec: 1.01x slower                                                 |
| pickle               | 11.7 us                                                                | 11.8 us: 1.01x slower                                                  |
| pickle_dict          | 34.2 us                                                                | 35.4 us: 1.03x slower                                                  |
| pickle_list          | 4.96 us                                                                | 5.28 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (5): xml_etree_parse, xml_etree_process, xml_etree_iterparse, unpickle_list, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.1 ms                                                                | 11.0 ms: 1.00x faster                                                  |
| python_startup_no_site | 9.52 ms                                                                | 9.51 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 54.5 ms                                                                | 53.7 ms: 1.01x faster                                                  |
| mako           | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                                  |
| genshi_text    | 24.7 ms                                                                | 25.0 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|--------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle                 | 17.4 us                                                                | 15.0 us: 1.16x faster                                                  |
| scimark_sor              | 141 ms                                                                 | 134 ms: 1.05x faster                                                   |
| gc_traversal             | 4.04 ms                                                                | 3.88 ms: 1.04x faster                                                  |
| deepcopy_memo            | 39.5 us                                                                | 38.5 us: 1.02x faster                                                  |
| asyncio_tcp              | 513 ms                                                                 | 501 ms: 1.02x faster                                                   |
| scimark_sparse_mat_mult  | 5.02 ms                                                                | 4.93 ms: 1.02x faster                                                  |
| logging_simple           | 5.94 us                                                                | 5.84 us: 1.02x faster                                                  |
| genshi_xml               | 54.5 ms                                                                | 53.7 ms: 1.01x faster                                                  |
| pyflate                  | 476 ms                                                                 | 471 ms: 1.01x faster                                                   |
| typing_runtime_protocols | 115 us                                                                 | 113 us: 1.01x faster                                                   |
| deepcopy                 | 366 us                                                                 | 362 us: 1.01x faster                                                   |
| json_loads               | 28.4 us                                                                | 28.2 us: 1.01x faster                                                  |
| generators               | 30.0 ms                                                                | 29.8 ms: 1.01x faster                                                  |
| thrift                   | 825 us                                                                 | 820 us: 1.01x faster                                                   |
| asyncio_tcp_ssl          | 1.86 sec                                                               | 1.85 sec: 1.01x faster                                                 |
| json_dumps               | 10.4 ms                                                                | 10.4 ms: 1.00x faster                                                  |
| unpickle_pure_python     | 242 us                                                                 | 240 us: 1.00x faster                                                   |
| python_startup           | 11.1 ms                                                                | 11.0 ms: 1.00x faster                                                  |
| xml_etree_generate       | 88.0 ms                                                                | 87.7 ms: 1.00x faster                                                  |
| python_startup_no_site   | 9.52 ms                                                                | 9.51 ms: 1.00x faster                                                  |
| pylint                   | 295 ms                                                                 | 296 ms: 1.00x slower                                                   |
| sqlglot_transpile        | 1.65 ms                                                                | 1.65 ms: 1.00x slower                                                  |
| docutils                 | 2.92 sec                                                               | 2.94 sec: 1.00x slower                                                 |
| create_gc_cycles         | 1.75 ms                                                                | 1.76 ms: 1.00x slower                                                  |
| sympy_sum                | 167 ms                                                                 | 168 ms: 1.00x slower                                                   |
| richards_super           | 49.5 ms                                                                | 49.8 ms: 1.01x slower                                                  |
| sympy_str                | 296 ms                                                                 | 298 ms: 1.01x slower                                                   |
| hexiom                   | 6.99 ms                                                                | 7.04 ms: 1.01x slower                                                  |
| aiohttp                  | 1.20 ms                                                                | 1.21 ms: 1.01x slower                                                  |
| tomli_loads              | 2.05 sec                                                               | 2.07 sec: 1.01x slower                                                 |
| sympy_integrate          | 22.0 ms                                                                | 22.2 ms: 1.01x slower                                                  |
| sympy_expand             | 494 ms                                                                 | 498 ms: 1.01x slower                                                   |
| mako                     | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                                  |
| richards                 | 43.6 ms                                                                | 44.1 ms: 1.01x slower                                                  |
| pickle                   | 11.7 us                                                                | 11.8 us: 1.01x slower                                                  |
| scimark_fft              | 345 ms                                                                 | 349 ms: 1.01x slower                                                   |
| nqueens                  | 89.8 ms                                                                | 90.9 ms: 1.01x slower                                                  |
| float                    | 77.3 ms                                                                | 78.4 ms: 1.01x slower                                                  |
| genshi_text              | 24.7 ms                                                                | 25.0 ms: 1.01x slower                                                  |
| regex_compile            | 143 ms                                                                 | 145 ms: 1.02x slower                                                   |
| go                       | 154 ms                                                                 | 157 ms: 1.02x slower                                                   |
| regex_effbot             | 3.73 ms                                                                | 3.80 ms: 1.02x slower                                                  |
| regex_dna                | 225 ms                                                                 | 230 ms: 1.02x slower                                                   |
| mdp                      | 2.77 sec                                                               | 2.83 sec: 1.02x slower                                                 |
| meteor_contest           | 110 ms                                                                 | 113 ms: 1.02x slower                                                   |
| pprint_safe_repr         | 743 ms                                                                 | 762 ms: 1.02x slower                                                   |
| html5lib                 | 66.7 ms                                                                | 68.5 ms: 1.03x slower                                                  |
| logging_silent           | 100 ns                                                                 | 103 ns: 1.03x slower                                                   |
| pickle_dict              | 34.2 us                                                                | 35.4 us: 1.03x slower                                                  |
| pycparser                | 1.18 sec                                                               | 1.23 sec: 1.04x slower                                                 |
| regex_v8                 | 25.0 ms                                                                | 26.0 ms: 1.04x slower                                                  |
| pprint_pformat           | 1.52 sec                                                               | 1.58 sec: 1.04x slower                                                 |
| pickle_list              | 4.96 us                                                                | 5.28 us: 1.06x slower                                                  |
| pidigits                 | 189 ms                                                                 | 211 ms: 1.11x slower                                                   |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (45): xml_etree_parse, deltablue, nbody, spectral_norm, scimark_monte_carlo, comprehensions, deepcopy_reduce, xml_etree_process, pathlib, tornado_http, fannkuch, xml_etree_iterparse, sqlglot_optimize, coroutines, bench_mp_pool, json, chaos, asyncio_websockets, gunicorn, dask, sqlglot_parse, chameleon, bench_thread_pool, mypy2, sqlite_synth, async_generators, dulwich_log, unpickle_list, raytrace, 2to3, telco, logging_format, pickle_pure_python, sqlglot_normalize, async_tree_cpu_io_mixed, scimark_lu, coverage, crypto_pyaes, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_none, async_tree_none_tg, async_tree_io_tg, async_tree_io

# HPT report

- Reliability score: 99.75% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x