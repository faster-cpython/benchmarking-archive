# Results vs. base

- fork: savannahostrowski
- ref: llvm_18
- machine: linux-x86_64
- commit hash: fe17f68
- commit date: 2024-04-26
- overall geometric mean: 1.00x faster
- HPT reliability: 97.83%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 281 ms                                                                 | 280 ms: 1.00x faster                                                 |
| html5lib       | 68.3 ms                                                                | 68.5 ms: 1.00x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (3): chameleon, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_io_tg, async_tree_none, async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 76.1 ms                                                                | 76.5 ms: 1.00x slower                                                |
| nbody          | 89.1 ms                                                                | 90.9 ms: 1.02x slower                                                |
| pidigits       | 198 ms                                                                 | 210 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.74 ms                                                                | 3.62 ms: 1.03x faster                                                |
| regex_compile  | 141 ms                                                                 | 140 ms: 1.01x faster                                                 |
| regex_dna      | 220 ms                                                                 | 223 ms: 1.02x slower                                                 |
| regex_v8       | 24.5 ms                                                                | 25.2 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 237 us                                                                 | 231 us: 1.02x faster                                                 |
| pickle_list          | 5.13 us                                                                | 5.02 us: 1.02x faster                                                |
| json_dumps           | 10.6 ms                                                                | 10.6 ms: 1.01x faster                                                |
| xml_etree_iterparse  | 103 ms                                                                 | 103 ms: 1.01x faster                                                 |
| pickle_pure_python   | 308 us                                                                 | 306 us: 1.01x faster                                                 |
| xml_etree_generate   | 87.8 ms                                                                | 87.5 ms: 1.00x faster                                                |
| unpickle_list        | 5.23 us                                                                | 5.27 us: 1.01x slower                                                |
| xml_etree_parse      | 149 ms                                                                 | 151 ms: 1.01x slower                                                 |
| pickle_dict          | 34.5 us                                                                | 35.0 us: 1.02x slower                                                |
| pickle               | 11.7 us                                                                | 11.9 us: 1.02x slower                                                |
| unpickle             | 15.3 us                                                                | 16.4 us: 1.07x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (3): json_loads, xml_etree_process, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                |
| python_startup_no_site | 7.65 ms                                                                | 7.63 ms: 1.00x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 10.7 ms                                                                | 10.4 ms: 1.03x faster                                                |
| django_template | 37.0 ms                                                                | 36.8 ms: 1.00x faster                                                |
| genshi_text     | 25.5 ms                                                                | 25.7 ms: 1.01x slower                                                |
| genshi_xml      | 56.5 ms                                                                | 57.2 ms: 1.01x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| scimark_sor              | 140 ms                                                                 | 131 ms: 1.06x faster                                                 |
| mdp                      | 2.80 sec                                                               | 2.63 sec: 1.06x faster                                               |
| fannkuch                 | 387 ms                                                                 | 372 ms: 1.04x faster                                                 |
| hexiom                   | 7.15 ms                                                                | 6.90 ms: 1.04x faster                                                |
| pprint_safe_repr         | 769 ms                                                                 | 744 ms: 1.03x faster                                                 |
| regex_effbot             | 3.74 ms                                                                | 3.62 ms: 1.03x faster                                                |
| richards_super           | 49.8 ms                                                                | 48.5 ms: 1.03x faster                                                |
| mako                     | 10.7 ms                                                                | 10.4 ms: 1.03x faster                                                |
| scimark_monte_carlo      | 69.5 ms                                                                | 67.8 ms: 1.02x faster                                                |
| richards                 | 43.4 ms                                                                | 42.4 ms: 1.02x faster                                                |
| unpickle_pure_python     | 237 us                                                                 | 231 us: 1.02x faster                                                 |
| pickle_list              | 5.13 us                                                                | 5.02 us: 1.02x faster                                                |
| spectral_norm            | 112 ms                                                                 | 109 ms: 1.02x faster                                                 |
| comprehensions           | 18.3 us                                                                | 18.0 us: 1.02x faster                                                |
| pprint_pformat           | 1.55 sec                                                               | 1.52 sec: 1.02x faster                                               |
| sqlglot_normalize        | 115 ms                                                                 | 113 ms: 1.02x faster                                                 |
| logging_simple           | 5.99 us                                                                | 5.89 us: 1.02x faster                                                |
| telco                    | 8.63 ms                                                                | 8.48 ms: 1.02x faster                                                |
| coverage                 | 94.0 ms                                                                | 92.6 ms: 1.02x faster                                                |
| sqlglot_optimize         | 58.2 ms                                                                | 57.4 ms: 1.01x faster                                                |
| go                       | 157 ms                                                                 | 155 ms: 1.01x faster                                                 |
| typing_runtime_protocols | 175 us                                                                 | 173 us: 1.01x faster                                                 |
| sympy_sum                | 170 ms                                                                 | 168 ms: 1.01x faster                                                 |
| logging_format           | 6.59 us                                                                | 6.52 us: 1.01x faster                                                |
| logging_silent           | 102 ns                                                                 | 101 ns: 1.01x faster                                                 |
| sqlglot_transpile        | 1.66 ms                                                                | 1.65 ms: 1.01x faster                                                |
| sympy_str                | 299 ms                                                                 | 297 ms: 1.01x faster                                                 |
| meteor_contest           | 112 ms                                                                 | 111 ms: 1.01x faster                                                 |
| sympy_integrate          | 22.5 ms                                                                | 22.3 ms: 1.01x faster                                                |
| sympy_expand             | 502 ms                                                                 | 498 ms: 1.01x faster                                                 |
| json_dumps               | 10.6 ms                                                                | 10.6 ms: 1.01x faster                                                |
| regex_compile            | 141 ms                                                                 | 140 ms: 1.01x faster                                                 |
| xml_etree_iterparse      | 103 ms                                                                 | 103 ms: 1.01x faster                                                 |
| asyncio_websockets       | 567 ms                                                                 | 564 ms: 1.01x faster                                                 |
| pickle_pure_python       | 308 us                                                                 | 306 us: 1.01x faster                                                 |
| django_template          | 37.0 ms                                                                | 36.8 ms: 1.00x faster                                                |
| 2to3                     | 281 ms                                                                 | 280 ms: 1.00x faster                                                 |
| raytrace                 | 279 ms                                                                 | 278 ms: 1.00x faster                                                 |
| xml_etree_generate       | 87.8 ms                                                                | 87.5 ms: 1.00x faster                                                |
| create_gc_cycles         | 1.78 ms                                                                | 1.77 ms: 1.00x faster                                                |
| python_startup           | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                |
| python_startup_no_site   | 7.65 ms                                                                | 7.63 ms: 1.00x faster                                                |
| html5lib                 | 68.3 ms                                                                | 68.5 ms: 1.00x slower                                                |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.86 sec: 1.00x slower                                               |
| float                    | 76.1 ms                                                                | 76.5 ms: 1.00x slower                                                |
| gc_traversal             | 3.77 ms                                                                | 3.79 ms: 1.01x slower                                                |
| genshi_text              | 25.5 ms                                                                | 25.7 ms: 1.01x slower                                                |
| async_generators         | 462 ms                                                                 | 465 ms: 1.01x slower                                                 |
| scimark_sparse_mat_mult  | 4.89 ms                                                                | 4.93 ms: 1.01x slower                                                |
| unpickle_list            | 5.23 us                                                                | 5.27 us: 1.01x slower                                                |
| xml_etree_parse          | 149 ms                                                                 | 151 ms: 1.01x slower                                                 |
| genshi_xml               | 56.5 ms                                                                | 57.2 ms: 1.01x slower                                                |
| scimark_lu               | 132 ms                                                                 | 134 ms: 1.01x slower                                                 |
| pickle_dict              | 34.5 us                                                                | 35.0 us: 1.02x slower                                                |
| regex_dna                | 220 ms                                                                 | 223 ms: 1.02x slower                                                 |
| pyflate                  | 458 ms                                                                 | 468 ms: 1.02x slower                                                 |
| nbody                    | 89.1 ms                                                                | 90.9 ms: 1.02x slower                                                |
| pickle                   | 11.7 us                                                                | 11.9 us: 1.02x slower                                                |
| deltablue                | 3.79 ms                                                                | 3.89 ms: 1.03x slower                                                |
| coroutines               | 22.7 ms                                                                | 23.3 ms: 1.03x slower                                                |
| regex_v8                 | 24.5 ms                                                                | 25.2 ms: 1.03x slower                                                |
| pidigits                 | 198 ms                                                                 | 210 ms: 1.06x slower                                                 |
| unpickle                 | 15.3 us                                                                | 16.4 us: 1.07x slower                                                |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (38): async_tree_memoization, json, crypto_pyaes, chaos, pylint, mypy2, bench_mp_pool, async_tree_io_tg, async_tree_none, sqlglot_parse, deepcopy_reduce, docutils, json_loads, bench_thread_pool, generators, dask, async_tree_io, tornado_http, gunicorn, dulwich_log, deepcopy_memo, xml_etree_process, deepcopy, chameleon, nqueens, sqlite_synth, async_tree_cpu_io_mixed, async_tree_memoization_tg, aiohttp, asyncio_tcp, async_tree_cpu_io_mixed_tg, scimark_fft, djangocms, tomli_loads, thrift, pathlib, pycparser, async_tree_none_tg

# HPT report

- Reliability score: 97.83% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x