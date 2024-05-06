# Results vs. base

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: linux-x86_64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 272 ms                                                                 | 268 ms: 1.01x faster                                                             |
| chameleon      | 6.95 ms                                                                | 6.74 ms: 1.03x faster                                                            |
| html5lib       | 67.9 ms                                                                | 66.9 ms: 1.01x faster                                                            |
| tornado_http   | 95.1 ms                                                                | 94.2 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization_tg, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_io, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 79.4 ms                                                                | 78.1 ms: 1.02x faster                                                            |
| nbody          | 89.6 ms                                                                | 88.6 ms: 1.01x faster                                                            |
| pidigits       | 193 ms                                                                 | 211 ms: 1.09x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                                 | 134 ms: 1.01x faster                                                             |
| regex_dna      | 227 ms                                                                 | 226 ms: 1.00x faster                                                             |
| regex_effbot   | 3.73 ms                                                                | 3.77 ms: 1.01x slower                                                            |
| regex_v8       | 25.8 ms                                                                | 26.2 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list        | 5.29 us                                                                | 5.15 us: 1.03x faster                                                            |
| xml_etree_process    | 61.5 ms                                                                | 60.0 ms: 1.03x faster                                                            |
| unpickle_pure_python | 226 us                                                                 | 221 us: 1.02x faster                                                             |
| xml_etree_generate   | 88.6 ms                                                                | 87.2 ms: 1.02x faster                                                            |
| xml_etree_iterparse  | 107 ms                                                                 | 106 ms: 1.01x faster                                                             |
| pickle_pure_python   | 303 us                                                                 | 300 us: 1.01x faster                                                             |
| tomli_loads          | 2.19 sec                                                               | 2.17 sec: 1.01x faster                                                           |
| pickle_list          | 4.94 us                                                                | 4.90 us: 1.01x faster                                                            |
| pickle_dict          | 33.5 us                                                                | 33.7 us: 1.01x slower                                                            |
| unpickle             | 15.1 us                                                                | 15.2 us: 1.01x slower                                                            |
| json_dumps           | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| json_loads           | 28.4 us                                                                | 29.0 us: 1.02x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): xml_etree_parse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.6 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| python_startup_no_site | 9.01 ms                                                                | 8.97 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                                | 10.8 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| scimark_sparse_mat_mult  | 5.18 ms                                                                | 4.89 ms: 1.06x faster                                                            |
| deepcopy_memo            | 38.6 us                                                                | 36.7 us: 1.05x faster                                                            |
| pyflate                  | 472 ms                                                                 | 451 ms: 1.05x faster                                                             |
| telco                    | 8.85 ms                                                                | 8.46 ms: 1.05x faster                                                            |
| crypto_pyaes             | 76.2 ms                                                                | 73.1 ms: 1.04x faster                                                            |
| gc_traversal             | 3.94 ms                                                                | 3.78 ms: 1.04x faster                                                            |
| deltablue                | 3.24 ms                                                                | 3.13 ms: 1.04x faster                                                            |
| comprehensions           | 17.0 us                                                                | 16.4 us: 1.03x faster                                                            |
| go                       | 144 ms                                                                 | 139 ms: 1.03x faster                                                             |
| spectral_norm            | 115 ms                                                                 | 111 ms: 1.03x faster                                                             |
| chameleon                | 6.95 ms                                                                | 6.74 ms: 1.03x faster                                                            |
| logging_silent           | 104 ns                                                                 | 101 ns: 1.03x faster                                                             |
| unpickle_list            | 5.29 us                                                                | 5.15 us: 1.03x faster                                                            |
| chaos                    | 60.9 ms                                                                | 59.3 ms: 1.03x faster                                                            |
| raytrace                 | 266 ms                                                                 | 259 ms: 1.03x faster                                                             |
| xml_etree_process        | 61.5 ms                                                                | 60.0 ms: 1.03x faster                                                            |
| logging_simple           | 5.84 us                                                                | 5.70 us: 1.02x faster                                                            |
| richards                 | 47.8 ms                                                                | 46.7 ms: 1.02x faster                                                            |
| generators               | 30.0 ms                                                                | 29.3 ms: 1.02x faster                                                            |
| unpickle_pure_python     | 226 us                                                                 | 221 us: 1.02x faster                                                             |
| nqueens                  | 81.9 ms                                                                | 80.2 ms: 1.02x faster                                                            |
| fannkuch                 | 396 ms                                                                 | 389 ms: 1.02x faster                                                             |
| sqlglot_normalize        | 112 ms                                                                 | 110 ms: 1.02x faster                                                             |
| mako                     | 11.0 ms                                                                | 10.8 ms: 1.02x faster                                                            |
| sympy_integrate          | 20.6 ms                                                                | 20.2 ms: 1.02x faster                                                            |
| float                    | 79.4 ms                                                                | 78.1 ms: 1.02x faster                                                            |
| scimark_fft              | 372 ms                                                                 | 366 ms: 1.02x faster                                                             |
| xml_etree_generate       | 88.6 ms                                                                | 87.2 ms: 1.02x faster                                                            |
| sympy_str                | 282 ms                                                                 | 278 ms: 1.02x faster                                                             |
| sqlglot_transpile        | 1.60 ms                                                                | 1.58 ms: 1.02x faster                                                            |
| meteor_contest           | 110 ms                                                                 | 108 ms: 1.01x faster                                                             |
| sqlglot_parse            | 1.29 ms                                                                | 1.28 ms: 1.01x faster                                                            |
| html5lib                 | 67.9 ms                                                                | 66.9 ms: 1.01x faster                                                            |
| regex_compile            | 136 ms                                                                 | 134 ms: 1.01x faster                                                             |
| 2to3                     | 272 ms                                                                 | 268 ms: 1.01x faster                                                             |
| coverage                 | 99.7 ms                                                                | 98.5 ms: 1.01x faster                                                            |
| richards_super           | 53.3 ms                                                                | 52.7 ms: 1.01x faster                                                            |
| aiohttp                  | 1.18 ms                                                                | 1.16 ms: 1.01x faster                                                            |
| sqlglot_optimize         | 55.7 ms                                                                | 55.1 ms: 1.01x faster                                                            |
| hexiom                   | 6.30 ms                                                                | 6.23 ms: 1.01x faster                                                            |
| deepcopy                 | 358 us                                                                 | 354 us: 1.01x faster                                                             |
| nbody                    | 89.6 ms                                                                | 88.6 ms: 1.01x faster                                                            |
| xml_etree_iterparse      | 107 ms                                                                 | 106 ms: 1.01x faster                                                             |
| scimark_sor              | 123 ms                                                                 | 122 ms: 1.01x faster                                                             |
| sympy_expand             | 473 ms                                                                 | 469 ms: 1.01x faster                                                             |
| tornado_http             | 95.1 ms                                                                | 94.2 ms: 1.01x faster                                                            |
| sympy_sum                | 157 ms                                                                 | 155 ms: 1.01x faster                                                             |
| pickle_pure_python       | 303 us                                                                 | 300 us: 1.01x faster                                                             |
| bench_thread_pool        | 836 us                                                                 | 829 us: 1.01x faster                                                             |
| create_gc_cycles         | 1.75 ms                                                                | 1.73 ms: 1.01x faster                                                            |
| logging_format           | 6.40 us                                                                | 6.34 us: 1.01x faster                                                            |
| tomli_loads              | 2.19 sec                                                               | 2.17 sec: 1.01x faster                                                           |
| dulwich_log              | 67.5 ms                                                                | 67.0 ms: 1.01x faster                                                            |
| pickle_list              | 4.94 us                                                                | 4.90 us: 1.01x faster                                                            |
| pprint_pformat           | 1.53 sec                                                               | 1.52 sec: 1.01x faster                                                           |
| pprint_safe_repr         | 750 ms                                                                 | 745 ms: 1.01x faster                                                             |
| async_generators         | 449 ms                                                                 | 446 ms: 1.01x faster                                                             |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.84 sec: 1.01x faster                                                           |
| python_startup           | 10.6 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| python_startup_no_site   | 9.01 ms                                                                | 8.97 ms: 1.00x faster                                                            |
| pylint                   | 280 ms                                                                 | 278 ms: 1.00x faster                                                             |
| regex_dna                | 227 ms                                                                 | 226 ms: 1.00x faster                                                             |
| mdp                      | 2.77 sec                                                               | 2.76 sec: 1.00x faster                                                           |
| asyncio_tcp              | 508 ms                                                                 | 510 ms: 1.00x slower                                                             |
| pickle_dict              | 33.5 us                                                                | 33.7 us: 1.01x slower                                                            |
| deepcopy_reduce          | 3.16 us                                                                | 3.18 us: 1.01x slower                                                            |
| typing_runtime_protocols | 114 us                                                                 | 115 us: 1.01x slower                                                             |
| unpickle                 | 15.1 us                                                                | 15.2 us: 1.01x slower                                                            |
| json_dumps               | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| regex_effbot             | 3.73 ms                                                                | 3.77 ms: 1.01x slower                                                            |
| sqlite_synth             | 2.91 us                                                                | 2.94 us: 1.01x slower                                                            |
| regex_v8                 | 25.8 ms                                                                | 26.2 ms: 1.01x slower                                                            |
| json_loads               | 28.4 us                                                                | 29.0 us: 1.02x slower                                                            |
| coroutines               | 22.2 ms                                                                | 22.7 ms: 1.02x slower                                                            |
| thrift                   | 810 us                                                                 | 829 us: 1.02x slower                                                             |
| pidigits                 | 193 ms                                                                 | 211 ms: 1.09x slower                                                             |
| Geometric mean           | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (23): scimark_monte_carlo, dask, xml_etree_parse, scimark_lu, gunicorn, mypy2, asyncio_websockets, json, pathlib, bench_mp_pool, pickle, pycparser, docutils, genshi_xml, async_tree_memoization_tg, genshi_text, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_io, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x